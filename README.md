# Code Institute Stream One Project
 
This is a project website for Code Institute Full Stack Development course Stream One. It is a sample website for a walking group based in the south-west of England, a small group which organises monthly walks in Devon and Cornwall both on moorland and along the coast path. The available version of the site presents a snapshot as it would have looked on 10 November 2017, at the end of the major development process.

The website provides information for both existing and potential group members. The site covers future events and past walks as well as information about the hobby of walking itself. The site also gives links to the group's social media accounts in the footer of each page. Because these accounts do not exist, the links direct to the home page of the relevant site.

## Responsive Design

There is one breakpoint set which is activated when the page width exceeds 800px. This switches from a horizontal menu to a vertical menu and also changes the header and footer text from left to centre aligned.

On the Home Page, Flexbox is used to arrange the information boxes and a minimum width of 250 pixels is set to ensure that the boxes do not become too narrow. Should the page width be such that the boxes would drop below 250 pixels, the furthest box to the right will drop below the others. Flexbox is also used in the membership form to show the two fieldsets alongside each other in the desktop display.

On the Upcoming Walks and Photo Galleries pages, the flex direction is initially set to column, in order to display two sections of content one above the other. In the desktop stylesheet, the direction is altered to row in order to show the two sections side by side.

## JavaScript Functionality

JavaScript is used on the Home Page to run the image switcher on the header image. A validation script is used for both the quick contact form on the Home Page and the membership form on the Join the Group page. These alert the user if a required field has been left empty, or confirm submission of the form if it has been filled in correctly.

Further use of JavaScript is made on the Upcoming Walks and Photo Galleries pages by the inclusion of a content switcher. That script loads by default the details of the next or most recent walk. There are links provided which when clicked, use a JavaScript function to display the details of a chosen walk while hiding all the others.

The Photo Galleries page also features a lightbox-style script which allows a user to click a thumbnail image and display it at a larger size in the centre of the viewport. The script includes a function to allow the user to move to either the previous or next image in the current gallery and a 'close' function to remove the image viewer.

External scripts are used in the context of the OS Openspace API on both the Home Page and the Upcoming Walks page. One of these is accessed remotely from the OS Openspace website, the other is generated using OS Openspace Map Builder and is stored with the site's other JavaScript files.

## File Structure

All image files, CSS files and JavaScript files are separated into different directories for clarity and simplicity. Images are further separated depending upon where in the site they are used.

## Site Content

### Home Page

The Home Page shows a header image of a past walk above a brief introductory paragraph. The header image uses JavaScript to rotate between a selection of images. The file size of these images has been reduced with the intention of improving the loading time of the page while not compromising the quality of the photographs. Below the introductory paragraph are three information boxes.

* The first of these shows the date of the next walk and a brief description of the route, along with a small map showing the starting point. There is a link to the Future Walks page where full details can be found.

* The second information box gives information about the most recent walk and a preview photo, with a link to the Photo Galleries page where more pictures are available.

* The final information box includes a simple contact form, for people who may not wish to join the group but who have an enquiry to send to the group organisers. The form just gives fields for basic contact information and a textbox for the message. As the scope of this project is front end only, the form does not submit but displays a validation message when the 'Send Message' button is clicked. This message either gives a warning if a required field has been left empty or confirms successful submission of the form.

### Upcoming Walks

The page detailing upcoming walks shows a brief description of the next route, along with a map of the route created using Ordnance Survey (OS) Openspace Map Builder and embedded using the OS Openspace API. The next scheduled walk is displayed by default, with a menu to enable the user to switch between the routes planned for the next six months. The menu links feature an image from along the planned route, giving the user a preview of one place which they would visit should they decide to go on that walk.

Enabling this functionality proved tricky to begin with so a separate GitHub branch was utilised until such time as the script was working satisfactorily.

### Photo Galleries

The galleries page gives a brief recap of the most recent walk, along with a short gallery of photos taken along the route. By default, the most recent walk will load first. Thumbnail versions of the full images are used to improve the loading time of the page. There is a menu identical to that on the Upcoming Walks page, enabling the user to switch between all the available galleries. The menu links again feature a background image, this time the first image from the gallery for that month.

There is also a lightbox script which enables photos to be viewed at a larger size. When the script is activated, the larger image loads over the page. There are 'previous' and 'next' links to navigate between the pictures in the current gallery and a link to close the viewer. The 'previous' and 'next' links are disabled on the first and last pictures in a gallery respectively.

### Walking Advice

The Walking Advice page is primarily aimed at people who are new to the hobby. It is the most static page on the website and simply provides a basic introduction to walking. The text explains what clothing and equipment might be needed in order to ensure a safe and comfortable day out walking.

### Join the Group

There is a specific page on the site for people who wish to join the group, which features a more detailed membership form. The form collects e-mail, telephone and postal contact details as well as asking about people's experiences of and preferences for walking. Such information can then be used to plan both the schedule of walks and the arrangement of transport to and from the starting point.

As with the contact form on the Home Page, the form does not submit as the scope of this project is front end only. It gives the same validation message when the button is clicked, either giving a warning if a required field has been left empty or confirming successful submission of the form. Additionally, some further messages are set which will be shown if a particular option has been chosen in the form. This allows group organisers to provide information which may be of interest to the person who is joining. Only the first applicable message will be shown in order to prevent the alert from being excessively large.

## External Code

Use of external code was made through the OS Openspace maps. Using these maps in the website requires the inclusion of one external JavaScript file, hosted by OS Openspace, which generates the maps. Additionally, the Openspace Map Builder generates JavaScript code which sets the centre point of the map and if required displays the planned route as a line on the map. Once generated, this code needs to be stored on the website server in a separate JavaScript file.

## Deployment

The site was deployed to GitHub pages very early in its development. The chief reason for this was to enable easy testing on other devices, specifically tablet and mobile, as development was being done on a PC. Once a new piece of functionality had been added and tested on a variety of browsers, a new commit was made to GitHub ensuring that the 'gh-pages' branch was up to date at all times.

## Testing

The site was tested on a variety of devices and on a number of different browsers. The site was developed primarily using Chrome on a Windows 10 PC, while further testing was done on the PC using Firefox and Microsoft Edge. The site was tested on smaller devices, both tablet and mobile phone, both running Android. Testing on these devices included using the Android versions of both Chrome and Firefox.

In the context of the functionality of the site, both the simple contact form on the Home Page and the membership form on the Join the Group page required testing to ensure that the correct validation message would be displayed. Both were tested with and without input in the required fields, ensuring that the failure message would be shown if any one of the required fields was left blank. The membership form was further tested with a variety of inputs in the 'Walking Details' fieldset, to ensure that the correct information message would be displayed if the user selected any of the inputs which had a message attached.

During the testing process, an issue was encountered whereby white space was showing below the month switcher menu on the Photo Galleries page. This was only happening on the mobile stylesheet on Chrome for Android, and only when either there were more than two month links above or the explanatory paragraph appeared below. The testing process did not produce any explanation for this white space and so it is currently assumed to be a bug in the browser.