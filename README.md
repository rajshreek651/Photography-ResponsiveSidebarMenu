# Photography-ResponsiveSidebarMenu
This webpage shows a photography website which has a responsive sidebar menu with different options. This show how the responsiveness and other visual effects are added to real-time websites showcasing magnificent use of CSS.

## Understanding the HTML code

* .main-box --> contains the entire content

* #check --> for a checkbox, which will get ticked when the 'Hamburger' icon is clicked. This can be implemented as creating a <label> for 'check' inside which the 'Hamburger' icon is there.

* Similar thing can be implemented for 'X-mark' icon, present inside <label> for  'check'

* .sidebar_menu --> contains the complete sidebar and its contents


## Understanding the CSS code

.sidebar_menu{
    position: fixed;
    left: -300px; --> this will make it get out off the screen; COMMENT IT OUT WHEN DESIGNING THE SIDEBAR MENU
    height: 100vh;
    width: 300px;
    background-color: rgba(255,255,255,0.1);
    box-shadow: 0 0 6px rgba(255,255,255,0.5);
    transition: all 0.3s linear;
}

#### Imp Logic related to checkbox

1. 
#check{
    display: none;
}

2. 
'~' is the sibling selector & the sibling for the 'checkbox' are '.sidebar_menu' & '.btn_one i.e. Hamburger icon'.
#check:checked ~ .sidebar_menu{ 
    left: 0;
}

3. 
#check:checked ~ .btn_one{
    opacity: 0;
}
_________________________________________________________________

Now we want that When Hamburger icon is clicked, the sidebar appears,
#check:checked ~ .sidebar_menu{ 
    left: 0; --> before .sidebar_menu was given left: -300px
}

Then hide the 'Hamburger icon' ,
#check:checked ~ .btn_one{
    opacity: 0;
}
_________________________________________________________________
