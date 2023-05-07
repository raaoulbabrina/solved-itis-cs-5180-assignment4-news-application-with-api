Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment4-news-application-with-api
<br>
In this assignment we are going to develop a news application using the XML RSS feeds provided by CNN. The urls for the different news categories are shown in the below table.

<table width="624">

 <tbody>

  <tr>

   <td width="181"><strong>Category</strong></td>

   <td width="443"><strong>XML RSS feed</strong></td>

  </tr>

  <tr>

   <td width="181">Top Stories</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_topstories.rss">http://rss.cnn.com/rss/cnn_topstories.rss</a></td>

  </tr>

  <tr>

   <td width="181">World</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_world.rss">http://rss.cnn.com/rss/cnn_world.rss</a></td>

  </tr>

  <tr>

   <td width="181">U.S.</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_us.rss">http://rss.cnn.com/rss/cnn_us.rss</a></td>

  </tr>

  <tr>

   <td width="181">Business</td>

   <td width="443"><a href="http://rss.cnn.com/rss/money_latest.rss">http://rss.cnn.com/rss/money_latest.rss</a></td>

  </tr>

  <tr>

   <td width="181">Politics</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_allpolitics.rss">http://rss.cnn.com/rss/cnn_allpolitics.rss</a></td>

  </tr>

  <tr>

   <td width="181">Technology</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_tech.rss">http://rss.cnn.com/rss/cnn_tech.rss</a></td>

  </tr>

  <tr>

   <td width="181">Health</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_health.rss">http://rss.cnn.com/rss/cnn_health.rss</a></td>

  </tr>

  <tr>

   <td width="181">Entertainment</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_showbiz.rss">http://rss.cnn.com/rss/cnn_showbiz.rss</a></td>

  </tr>

  <tr>

   <td width="181">Travel</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_travel.rss">http://rss.cnn.com/rss/cnn_travel.rss</a></td>

  </tr>

  <tr>

   <td width="181">Living</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_living.rss">http://rss.cnn.com/rss/cnn_living.rss</a></td>

  </tr>

  <tr>

   <td width="181">Most Recent</td>

   <td width="443"><a href="http://rss.cnn.com/rss/cnn_latest.rss">http://rss.cnn.com/rss/cnn_latest.rss</a></td>

  </tr>

 </tbody>

</table>

<strong>Table 1. XML RSS feeds  </strong>

<strong>Connecting with the API </strong>

The interface should be created to match the user interface (UI) presented in Figure 1. You will be using layout files, and strings.xml to create the user interface. Perform the following tasks:

<ol>

 <li>This app should use the XML RSS feeds listed in Table 1 based on the category selected by the user.</li>

 <li>Clicking on the “Go” Button should display a list of categories as shown in Figure 1.</li>

</ol>

You can either Alert Dialog or Spinner to implement it.

<ol start="3">

 <li>Clicking on a category should do the following:

  <ol>

   <li>The TextView will hold the search category clicked by the user.</li>

   <li>Use AsyncTask/Thread to connect to the corresponding XML RSS feed URL to retrieve and parse the XML returned for the selected category. The AsyncTask/ Thread class should be in a separate file/class not inner to the main thread. i.e. You should manage passing parameters to the class and then pass back the result image downloaded to the UI.</li>

  </ol></li>

 <li>When the api data is retrieved:

  <ol>

   <li>Display the first news item from the list of retrieved news items as shown in Figure 1.</li>

   <li>Use Picasso to retrieve and display the first image associated with the displayed news item and display it in the ImageView. The API will return several images for each news item, display only the first image for the displayed news item.</li>

  </ol></li>

 <li>The Next and Previous news item icons should be disabled when the application is launched, and enabled after the first news item is displayed. The buttons will also remain disabled in the case there is only 1 or 0 news items corresponding to the provided category. Use icons provided in Support Files for setting the image icons (<strong>png, prev.png</strong>)</li>

 <li><strong>Do not</strong> store the photos, simply download and display the retrieved photos. Also do not attempt to download all the URLs receive, and your app should only download and display a single news photo at any given time.</li>

 <li>Upon clicking the “Next” icon, you should display the next news item from the retrieved news items and download the news photo accordingly. If the currently displayed news item happens to be the last news item, you should display the news item at index 0 (first news item) and download the news photo accordingly.</li>

 <li>Clicking the “Previous” icon, you should display the previous new item from the retrieved news items and download the news photo accordingly. If the currently displayed news item happens to be the first news item, you should display the last news item and download the news photo accordingly.</li>

 <li>Notice the “1 out of 20” text at the bottom of the screen, this should be updated according to the currently displayed news item.</li>

 <li>If the api returns an empty list of news items then clear the currently displayed news item and display an error Toast message “No News Found”.</li>

 <li>Your application should connect with the api and download the requested photo only if there is an established internet connection. If there is no internet connection you should display a Toast message indicting that there is no internet connection and do not attempt to send the HTTP request.</li>

 <li>Upon clicking the image or the news title, open the news URL for the displayed news item in the emulator’s browser.</li>

</ol>

<strong>Figure 1, Application Wireframe</strong>