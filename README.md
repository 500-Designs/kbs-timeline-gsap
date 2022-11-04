

# KBS timeline template fix

Issue Details: https://500designs.monday.com/boards/2033393118/pulses/3410983542/posts/1773558676

Page to fix: https://kbsredesigndev.wpengine.com/

- This is update on recent Timeline Section to add a Button "Back to Chart View".
- Initial Codes are taken from source code pasted in the "HTML code" fields of Elementor template named "	
Timeline – Oldest Desktop". with shortcode: `[elementor-template id="9004111226264302"]`
- Dev site Link: [edit the template](https://kbsredesigndev.wpengine.com/wp-admin/post.php?post=9004111226264302&action=edit)


Fix Feature:

1. Add "Back to Chart View" button that resets all GSAP animations and go back to first slide
2. Make the button only appear when user scrolls to the last slide

- Refer to commits `b73e62a` and `4150fdb` for code reference on how the above features were implemented

Fix Limitations:

1. Make the button part of the graph, since all elements in graph is contained in svg.
2. Match figma mockup showing arrows at the bottom, unless the entire gsap animated SVG is reqbuilt from sratch. 


Additional fixes can be made just through html and css, without tackling the GSAP imeplementation

- adjust bottom spacing of the graph on large screen
- adjust size of Button

Screenshots:

Initial State / Chart View:

When mouse drag / click occurs inside the graph and users scrolls to the last slide: