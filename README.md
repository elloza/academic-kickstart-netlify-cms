# Academic Kickstart Netlify CMS
<p align="center">
  <img src="https://github.com/elloza/academic-kickstart-netlify-cms/blob/master/readmeimg/WeeklySourGuernseycow-size_restricted.gif">
</p>

## Description

This repository it based on the [Academic Theme Hugo](https://github.com/gcushen/hugo-academic). It has been integrated with NetlifyCMS and the following content has been added:

- [x] Posts
- [x] Publications
- [x] Projects 
- [x] Teaching
- [x] Contact
- [x] Talks

In addition, pages for the managments of the CMS' sections.


- [x] Global configuration
- [x] About
- [x] Contact
- [x] Posts
- [x] Projects
- [x] Publications
- [x] Publications selected
- [x] Tags
- [x] Teaching


The original template has been modified in order to match with the structure of pictures of Netlify CMS (almost all the changes are related to images path in the partials of the theme)


## Instructions

If you want to deploy this in NetlifyCMS easily, follow the next steps:

1. Deploying this repository in NetlifyCMS

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/elloza/academic-kickstart-netlify-cms)

2. Enable Identity service and Git Gateway

3. Add postprocessing script for admin zone access

  * Insert this before end of head:

  ```javascript
  <script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
  ```
  
  * Insert this code before end of body:

  ```javascript
  <script>
    if (window.netlifyIdentity) {
      window.netlifyIdentity.on("init", user => {
        if (!user) {
          window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
          });
        }
      });
    }
  </script>
  ```


4. Give access to users

5  Confirm email and set password 

6. Access  to your new site admin page with /admin 

7. In this section you can start editing your site


## WIP

- [ ] Bugs in the talks section
- [ ] Check carefully all fields

## Result

<p align="center">
  <img src="https://github.com/elloza/academic-kickstart-netlify-cms/blob/master/readmeimg/result.gif">
</p>

## References:

Thanks a lot to :

* Blog of [@ragasirtahk](https://github.com/ragasirtahk) --> [Blog](https://www.ragasirtahk.tk/)
* People of NetlifyCMS Gitter channel
