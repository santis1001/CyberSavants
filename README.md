# CyberSavants
02 Challenge Bootcamp

# Description
In this challenge, I showcase my portfolio by displaying a list of my work and personal information. I will be using what I have learned so far in the bootcamp to create this portfolio.

## Acceptance Criteria
Here are the critical requirements necessary to develop a portfolio that satisfies a typical hiring manager’s needs:

```
GIVEN I need to sample a potential employee's previous work
WHEN I load their portfolio
THEN I am presented with the developer's name, a recent photo or avatar, and links to sections about them, their work, and how to contact them
WHEN I click one of the links in the navigation
THEN the UI scrolls to the corresponding section
WHEN I click on the link to the section about their work
THEN the UI scrolls to a section with titled images of the developer's applications
WHEN I am presented with the developer's first application
THEN that application's image should be larger in size than the others
WHEN I click on the images of the applications
THEN I am taken to that deployed application
WHEN I resize the page or view the site on various screens and devices
THEN I am presented with a responsive layout that adapts to my viewport
```
# Screenshots

## Original sizing
![Original Video](./assets/screenshots/original.gif)
## Media screen Resize
![Resize Video](./assets/screenshots/media%20Sreen%20resize.gif)

## Navigation Code
### HTML
```html
<nav class="navigation">
                <div class="dropmenu">
                    <h3 class="menu">Menu</h3>
                </div>
                
                <ul class="container_nav">                    
                    <li id="am">
                        <div class="header_list_spacer" id="hcs1">
                            <div class="header_card_spacer" ></div>
                        </div>
                        <div class="header_card" >
                            <a href="#About_me">
                                <h3>About Me</h3>
                            </a>
                        </div>
                        <div class="header_list_spacer" id="hcs2">
                            <div class="header_card_spacer" ></div>
                        </div>
                    </li>
                    
                    <li id="ed">
                        <div class="header_list_spacer" id="hcs2_2">
                            <div class="header_card_spacer" ></div>
                        </div>
                        <div class="header_card" >
                            <a href="#Education">
                                <h3>Education</h3>
                            </a>
                        </div>
                        <div class="header_list_spacer" id="hcs3">
                            <div class="header_card_spacer"></div>
                        </div>  
                    </li>                                                          
                    <li id="sk">    
                        <div class="header_list_spacer" id="hcs3_2">
                            <div class="header_card_spacer"></div>
                        </div>                          
                        <div class="header_card" >
                            <a href="#Skill">
                                <h3>Skills</h3>
                            </a>
                        </div>
                        <div class="header_list_spacer" id="hcs4">
                            <div class="header_card_spacer" ></div>
                        </div>
                    </li>
                    
                    <li id="wk">
                        <div class="header_list_spacer" id="hcs4_2">
                            <div class="header_card_spacer" ></div>
                        </div>
                        <div class="header_card">
                            <a href="#Work">
                                <h3>Work</h3>
                            </a>
                        </div> 
                        <div class="header_list_spacer" id="hcs5">
                            <div class="header_card_spacer"></div>
                        </div>                       
                    </li>
                    
                    <li id="eh">
                        <div class="header_list_spacer" id="hcs5_2">
                            <div class="header_card_spacer"></div>
                        </div>
                        <div class="header_card">
                            <a href="#Employment_History">
                                <h3>Employment History</h3>
                            </a>
                        </div>    
                        <div class="header_list_spacer" id="hcs6">   
                            <div class="header_card_spacer"></div>
                        </div>   
                    </li>    
                                
                </ul>
            </nav>
```
### CSS
```css
/* Navigation  */
nav{    
    display: flex;
    width: 65%;
    height: 68px;    
    flex-direction: row;
    flex-wrap: wrap;
}
/* dropmenu */
.dropmenu{
    display: none;
}
/* spacing and width  */
nav>ul {
    display: flex; 
    margin-right: 0%;
    min-width: 250px;
    height: 100%;;
    background-color: var(--theme);
}
nav ul li{
    display: flex;
    height: 100%;;
    background-color: var(--theme);
    
}
.header_list_spacer{
    width: 20px; 
    height: 100%;
    background-color: var(--pink);
}

.header_card_spacer{
    width: 20px; 
    height: 100%;        
    background-color: var(--theme);
    transition: border-radius 0.5s ease;
}
.header_card{
    
    align-items: center;   

    height: 100%;
    border-radius: 40px 40px 0px 0px;

    background-color: var(--theme);
    transition: all 0.5s ease;
    
    background-image: linear-gradient(to top, var(--pink) 50%, var(--theme) 50%);
    background-position: top;
    background-size: 100% 200%;
    transition: background-position 0.5s ease-in-out;
}

nav a{
    display: flex; 
    align-items: center;   
    height: inherit;
    color: var(--white);
    transition: color 0.5s ease;
  
    margin-left: 5px;
    margin-right: 5px;

} 
 
/* Navigation Animation for About Me */

.container_nav #am:hover .header_card{
    background-color: var(--pink);
    background-position: bottom;
}
.container_nav #am:hover #hcs1 div{
    border-radius: 0px 0px 20px 0px;
} 
.container_nav #am:hover #hcs2 div{
    border-radius: 0px 0px 0px 20px;
} 

/* Navigation Animation for Education */
.container_nav #ed:hover .header_card{
    background-color: var(--pink);
    background-position: bottom;
}
.container_nav #ed:hover #hcs2_2 div{
    border-radius: 0px 0px 20px 0px;
} 
.container_nav #ed:hover #hcs3 div{
    border-radius: 0px 0px 0px 20px;
} 

/* Navigation Animation for Skills */
.container_nav #sk:hover .header_card{
    background-color: var(--pink);
    background-position: bottom;
}
.container_nav #sk:hover #hcs3_2 div{
    border-radius: 0px 0px 20px 0px;
} 
.container_nav #sk:hover #hcs4 div{
    border-radius: 0px 0px 0px 20px;
} 

/* Navigation Animation for Work*/
.container_nav #wk:hover .header_card{
    background-color: var(--pink);
    background-position: bottom;
}
.container_nav #wk:hover #hcs4_2 div{
    border-radius: 0px 0px 20px 0px;
} 
.container_nav #wk:hover #hcs5 div{
    border-radius: 0px 0px 0px 20px;
} 

/* Navigation Animation for Employment History */
.container_nav #eh:hover .header_card{
    background-color: var(--pink);
    background-position: bottom;
}
.container_nav #eh:hover #hcs5_2 div{
    border-radius: 0px 0px 20px 0px;
} 
.container_nav #eh:hover #hcs6 div{
    border-radius: 0px 0px 0px 20px;
} 
```
![navigation bar](./assets/screenshots/navigation.gif)


# Pages Link
Website Link [Github Pages Link](https://santis1001.github.io/CyberSavants/)
