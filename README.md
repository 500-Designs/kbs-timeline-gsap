

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

- Refer to commits [`b73e62a`](https://github.com/jamesdev500/kbs-timeline-gsap/commit/b73e62a76f0e2ca650d6c0bfc7f7cc1e121f533a) and [`4150fdb`](https://github.com/jamesdev500/kbs-timeline-gsap/commit/4150fdb632fff6c87de32e30aefbc2e45a80867e) for code reference on how the above features were implemented

Fix Limitations:

1. Make the button part of the graph, since all elements in graph is contained in svg.
2. Match figma mockup showing arrows at the bottom, unless the entire gsap animated SVG is reqbuilt from sratch. 


Additional fixes can be made just through html and css, without tackling the GSAP imeplementation

- adjust bottom spacing of the graph on large screen
- adjust size of Button

Screenshots:

Initial State / Chart View:
![alt text](https://raw.githubusercontent.com/jamesdev500/kbs-timeline-gsap/main/preview/chart-view.jpg)

When mouse drag / click occurs inside the graph and users scrolls to the last slide:

![alt text](https://raw.githubusercontent.com/jamesdev500/kbs-timeline-gsap/main/preview/timeline-last-slide.jpg)