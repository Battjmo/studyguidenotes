# HTML 5

pros

1. accessibility
  semanic html headings make screen readers do better
  ARIA: spec that give elements roles, like header and footer
  
 2. AV support
  <video> and <audio> tags to get rid of media players
  
 3. !DOCTYPE
  much simpler doctype declaration
  
 4. clean code
  semantic tags make code much more readable, like <nav> for navs
  
 5. storage
  allows local storage client-side
  
 6. interaction
  yeah it's canvas guy, lots of other good api's too:
    DnD
    offline storage
    browser history management
    document editing
    timed media playback
    
 7. gamedev
   can use canvas for gamz instead of flash
   
 8. legacy / cross browser support
   everyone can use it
   
 9. Mobile
    hella good mobile features:
      define viewport settings
      full screen browsing
      home screen icons
      
 10. it's the future my guy
 
 
 ---
 
 # Media Query
 css technique for responsive site design
 add breakpoints at diff sizes where css changes
 do mobile first, easier to scale up than down
 mobile, tablet, screen good settings
 alt: phone, portrait tablet, landscape tablet, laptop, monitor
 can also check for orientation
 can hide elements, change fonts, all the good ish
  
  ---
  # Grid
  
  it makes grids, guy
  
  3x2 grid 2/ widths on columns, heights on rows:
  
  .wrapper {
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-template-rows: 50px 50px;
}

can create cell that aren't filled, they just won't show up until they are

to mess with an individual item:

.item1 {
    grid-column-start: 1; // starts at beginning of column 1
    grid-column-end: 4; // ends at beginning of column 4, which doesn't exist, but represents the end of column 3
}

can also be:

.item1 {
    grid-column: 1 / 4;
}

can be negative indexed too

can also be define as a span:

grid-column-start: 2
grid-column-end: span 2

two cell wide instruction

can declare start a span to start from the end
