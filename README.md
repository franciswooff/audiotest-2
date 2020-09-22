# audiotest
Template for School of Science, Engineering & the Environment students at the University of Salford to adapt to host comparative audio tests online.
THIS VERSION IS NOW LARGELY DEPRECIATED. The main branch of this repository uses an embedded video player to solve issues with poor browser support of switching audio tracks during playback of the html video element. Only use this version (which does this) if you wish to avoid use of the embedded Vidyard player in the main branch. At last test this version works on Safari & Edge (84). It does not currently work in Chrome without specific developer flags enabled. The .mov video codec used here does not work for Firefox, an .mp4 video would show, but it has not yet been tested if audio track switching will work with his codec.
latest update 22/9/20 9:50

To use this template the following additional actions are required as a minimum:

1. A video file with multiple audio tracks to switch between should accompany the other files (html, css, js & php) in the directory. The video file referenced in the html files currently is “output2.mov”, this reference will need to be edited to match the video file you are using. If using a different video codec it may also be necessary to amend "type="video/quicktime"" as appropriate.
2. When the php file(s - one per test page, see point 6 below) are performing their function they e-mail test results to an address “hard written” into the code of the files. Currently placeholder address "you@edu.salford.ac.uk" is used, this will need to be edited to the test owner's e-mail address.
3. The php file(s) need to be hosted on a machine running PHP (e.g. a web server) to perform their function. You could test and develop the function of the html, css & js files hosting these locally, but the functionality that follows pressing “Submit” on the html page(s) will not work. See University Service Portal Knowledge article https://salfordprod.service-now.com/sp?id=search&q=KB0010645 for information on University provided hosting accounts.

The following further steps may be needed to adapt the project for your use:

6. For each additional test page you will need differently named copies of index.html & form2mail.php. One example copy of each is included in this repository, with the copy pages named page2.html & form2mail2.php respectively. In addition to renaming the copied html file(s) & editing them to reference different video files, you will need to edit the "action" on the form included, so the test results are sent to the corresponding php file. You will need to edit the php file so the e-mail it sends has a different subject (p1, p2, p3 etc.) so you can tell which e-mail received relates to which test page. You will need to edit the link on the php page which takes you to the next page of the test (or back to the beginning, on the final page of the test).
7. You may need to create additional "faders" & buttons if you have more than 3 audio tracks per test video/page. Currently this involves:
- Editing the html file(s) by adding (copy & paste insert) more "channel" divs to the "panel" div, adding extra labels & inputs to the form & changing "a", "b" etc. in the copied elements to ""d", "e" etc. (3 places for each added channel & form element pair).
- Editing the php file(s) to receive a greater number of inputs from the html form & mail these.
- It is no longer necessary to edit the .js file (or the .css file, unless you wish to change the look of your test)
8. Consideration should be given to GDPR regulation, despite the very small amount of data being collected (name of subject) in running the test. You might consider removing the text input field for name from the test to anonymise it, removing personal data from the test, but as the page will be hosted on the net & searchable & accessible to anyone this runs the risk of random & possibly unreliable results.
