# Front-end Coding Standards and Best Practices

This document contains guidelines and best practices for the front-end development team at Backbone.

## Overview

The goals for creating this document are to:

- Produce code of a consistent quality across all projects / offices
- Streamline process for collaborating with multiple developers or agencies on the same project at the same time in the same way
- Write dynamic code that can evolve and grow
- Produce code that is less prone to bugs and regressions, is easier to understand and debug

This document will be updated regulary to reflect development trends and to suit the needs of what we do at Backbone.

## General Development Standards

For all projects:

- Consistency and naming conventions between team members is crucial. Developer must ensure that all codes/comments can be reasonably easy to interprete and pick-up by other team members.
- Solutions should be as simple and clear as possible. They should serve specific purpose and can be maintain or expand over time.

### Code Consistency

The usage of the same development pattern is critical and beneficial to our team members. It allows us to quickly understand code, provide or implmenent solutions. It also simplifies debugging which, as a result, speeds up development process.

It is highly recommended to establish environments, tools used before or at the start of a project.

### Performance

Page load times are a key consideration for users of all browsers and device types. The following improves page load performance:

- Reduce the amount of HTTP requests
- Minify all your files, compress all your assets before uploading to server
- Lazy load content when possible
- Regulary benchmark your site using tools such as Google Page Speed, Lighthouse etc. then follow their recommendations

### Keep your code DRY (Don't Repeat Yourself)

If you find yourself repeating code snippet you already made, refactor it so that it only has one representation in the codebase. With this principle, you will ensure that there is only one place to ever update or maintain your code.

### Keep your code simple

When writing code or planning for solutions, it is best to always take the most simple, basic approach. Split your code into small functions that each is responsible for one task. This allows them to be easy for debugging and they can also be reused if necessary.

### Testing and QA

Always test your code and make sure, as much as possible, you have tested on a reasonable number of devices so you can catch problems before you commit or deploy to your project. Do not rely on testers or other team members to catch issues for you as this will lengthen the development time.

## Requirements for Libraries, Frameworks, and Plugins

Use the following libraries and frameworks when developing your project:

- Grid Framework: Bootstrap current: 5.0.2 (https://getbootstrap.com/docs/5.0/getting-started/introduction/)
- Sliders and galleries: Swiper JS (https://swiperjs.com/)
- Form validations: Validate JS https://jqueryvalidation.org/documentation/
- Form input masks: https://github.com/RobinHerbots/Inputmask

Others (optional)

- Platforma 2 (https://platforma.ws/)
- Font Awesome Pro (https://fontawesome.com/v5.15/icons)
- MVC: Vue JS, React JS, Next JS
- Tailwind CSS
- jQuery
- Core UI Pro

## Development with Expresia

Some tips and best practices to follow when developing your project with Expresia.

### Fetch your data from API efficiently 

- Only hydrate data that you need for your page
- Make use of "noUnhydrated=1" to reduce payload size
- Always be mindful of the amount of API requests, some can be shared across elements, ensure there is no duplicated Data sources.
- Don't forget your params! Some query parameter are crucial but easy to forget i.e. a check for object status when rendering a collection (e.g. always set Active and Visible params when displaying a list of articles/sections), consider best sorting options based on your content, additional parans for multi-language maybe required for your project
- Consider the length of data on your page when it grows over time. Use pagination to avoid fetching a big chunk of data.

### Working with Playlists

All playlist skins should be able to: 

- Handle content dynamically and be able to grow over time.
- Appear anywhere on a page in any direction and still look and function properly
- Have multiple of the same skin on a page. Use playlist Id as identifier to avoid errors in your Javascript or HTML
- Change its appearance or minor customizations by using playlist options

### Other misc. tips

- Avoid using too many XprLogic in an element
- Avoid nesting multiple levels of elements
- Use try / catch in your Javascript
- Clean up unused elements, data sources, SSJS etc.

