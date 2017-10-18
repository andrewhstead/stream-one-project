# Code Institute Stream One Project
 
This is a project website for Code Institute Full Stack Development course Stream One. It is a sample website for a walking group based in the south-west of England, a small group which organises monthly walks in Devon and Cornwall both on moorland and along the coast path. 

The website provides information for both existing and potential group members, covering future events and past walks as well as information about the hobby of walking itself.

## Responsive Design

There is currently one breakpoint set which is activated when the page width exceeds 800px. This switches from a horizontal menu to a vertical menu and also changes the header and footer text from left to centre aligned.

On the Home Page, Flexbox is used to arrange the information boxes and a minimum width of 200 pixels is set to ensure that the boxes do not become too narrow. Should the page width be such that the boxes would drop below 200 pixels, the further box to the right will drop below the others. Flexbox is also used in the membership form to show the two fieldsets alongside each other in the desktop display.

On the Upcoming Walks page, the flex direction is initially set to column, in order to display the walk description and map below the switcher menu. In the desktop stylesheet, the direction is altered to row in order to show the menu and details side by side.

## Site Content

### Home Page

The Home Page shows a header image of a past walk above a brief introductory paragraph. Below that are three information boxes.

* The first of these shows the date of the next walk and a brief description of the route, along with a small map showing the starting point. There is a link to the Future Walks page where full details can be found.

* The second information box gives information about the most recent walk and a preview photo, with a link to the Photo Galleries page where more pictures are available.

* The final information box includes a simple contact form, for people who may not wish to join the group but who have an enquiry to send to the group organisers. The form just gives fields for basic contact information and a textbox for the message.

### Upcoming Walks

The page detailing upcoming walks shows a brief description of the next schedule walk, along with a map of the route created using OS Openspace Map Builder and embedded using the Openspace API. There is a menu which allows the user to switch between this map and others in the upcoming schedule. The next walk always displays as default when the page loads.

### Walking Advice

The Walking Advice page is primarily aimed at people who are new to the hobby. It simply provides a basic introduction to walking, explaining what clothing and equipment might be needed in order to ensure a safe and comfortable day out.

### Join the Group

There is a specific page on the site for people who wish to join the group, which features a more detailed membership form. The form collects e-mail, telephone and postal contact details as well as asking about people's experiences of and preferences for walking. Such information can then be used to plan both the schedule of walks and the arrangement of transport to and from the starting point.