# AI Powered News Search App using IBM Cloud Services

# [Watch the video: Link](https://www.youtube.com/watch?v=7wZutVgPWuo&t=106s)
[![Watch the video: Link](https://user-images.githubusercontent.com/48029688/82014897-2d294c80-969b-11ea-94c1-2a4152a5b597.gif)](https://www.youtube.com/watch?v=QlzXNx46c6I)

The web is home to massive amounts of data, with more being created every day. Organizations can harness this constant stream of information to gain understanding, plan strategies, and find opportunities. Enriched news data can help your application make dynamic connections across current events faster.
This app allows the user to search for any news at any time. The Watson discovery service used has an inbuilt collection of news in various topics which brings news to the doorstep in a jiffy.

In this project, we’ll start with the basics and build our own news mining web application using Node-RED / Python Web App and the IBM Watson Discovery Service. 

To do this, we’ll:
1. Build a Server Side Application using Node-RED
2. Use the pre-built Watson Discovery News collection
3. Access the Watson Discovery Service through the Discovery API

Optionally, we can choose to:
1. Use a Slack interface to query the data
2. Push news alerts out to web notification
3. Deploy the app on IBM Cloud

This code pattern shows you how to tap into massive data sets to mine insight. The app demonstrates two use cases using Watson Discovery News:
* **Search:** Query for the most relevant new articles about a specific topic or subject. Because the news collection is pre-enriched with natural language processing, you can query not just on keywords or categories but also on concepts, sentiment, and relations to get richer search responses.
* **Trending topics in the news:** Identify popular topics over the past 24 hours. Topics can be general or specific to an industry or category.

We propose the use of IBM Discovery, IBM Watson and IBM Node-RED.

Discovery:

![image](https://user-images.githubusercontent.com/48029688/82014015-4fba6600-9699-11ea-89d8-016b5840a1b4.png)

![image](https://user-images.githubusercontent.com/48029688/82014302-f69f0200-9699-11ea-8e91-d16050f95a1c.png)

1. The user interacts with the app UI(Built with Node-RED or Cloud or Local) to request relevant news content.
2. The app sends user requests to Watson Discovery News.
3. The Watson Discovery Service is continually crawling the web to update its Discovery News collection.
4. The Watson Discovery Service responds to Slack search requests.

SOFTWARE:
* Code is written in Node.js, with the server-side using the Express framework and the client using ReactJS.
* The pre-built Watson Discovery News collection was used.
* Access the Watson Discovery Service through the Discovery API.
* Use a Slack interface to query the data

## FLOWCHART
![image](https://user-images.githubusercontent.com/48029688/82014730-d4f24a80-969a-11ea-931f-bee9d0ca39ad.png)

## Result
![AI_Smart1](https://user-images.githubusercontent.com/48029688/82014897-2d294c80-969b-11ea-94c1-2a4152a5b597.gif)

Node-Red Flow:

![image](https://user-images.githubusercontent.com/48029688/82016543-e3dafc00-969e-11ea-9b85-8f45271e6997.png)
![image](https://user-images.githubusercontent.com/48029688/82016528-df164800-969e-11ea-842b-a5fd799b1684.png)

Output:
Main Search Page:

![image](https://user-images.githubusercontent.com/48029688/82016641-1ab11200-969f-11ea-8c42-b403f5ce7358.png)
![image](https://user-images.githubusercontent.com/48029688/82016646-1dac0280-969f-11ea-96ef-14a30f0e6b5a.png)

Trending:

![image](https://user-images.githubusercontent.com/48029688/82016656-21d82000-969f-11ea-9d10-ce993635c0d1.png)

Slack Integration:

![image](https://user-images.githubusercontent.com/48029688/82016782-62d03480-969f-11ea-84a2-26c2b3016931.png)
![image](https://user-images.githubusercontent.com/48029688/82016791-65cb2500-969f-11ea-9612-3ef17aec8de0.png)
![image](https://user-images.githubusercontent.com/48029688/82016794-68c61580-969f-11ea-86a8-c7bac57f6fb9.png)

### Advantages and Disadvantages:
The following advantages and disadvantages are observed.

Advantages:

* Complete integration with Discovery, Twitter and Slack
* News coming with sentiment analysis done
* Singular commands needed for slack to get news
* Getting recent tweets real-time.
* Option to get trending news realtime

Disadvantages

* Currently only 3 search results, but that can be easily increased with more functions.
* Since it does store tweets and only displays recent ones, searching for non-popular keywords may find less occurent tweets.



### APPLICATIONS

* A full fledged software or website with real-time applications
* Getting news articles fast and reliable with score and other metadata informations
* Sentiment analysis on the data
* Can be used as an everyday-app to browse and get news real-time, anytime in the day

### CONCLUSION

So here, we created this application on the web with sentiment analysis, slack integration and embedded using Node-Red and Watson Discovery. 

### FUTURE SCOPE

* The future scope may include:
* Adding Watson assistant to it.
* News search using audio and converting that using speech-to-text.
* Using language translator to view news in regional languages.
* Adding language translator with audio to enable search and results in regional language.

Node-RED IBM Cloud Starter Application
====================================

### Node-RED on IBM Cloud

This repository is an example Node-RED application that can be deployed into
IBM Cloud with only a couple clicks. Try it out for yourself right now by clicking:

[![Deploy to IBM Cloud](https://cloud.ibm.com/devops/setup/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/ibm/node-red-app)

### How does this work?

When you click the button, you are taken to IBM Cloud where you get a pick a name
for your application at which point the platform takes over, grabs the code from
this repository and gets it deployed.

It will automatically create an instance of the Cloudant service and bind it to
your app. This is where your Node-RED instance will store its data.

When you first access the application, you'll be asked to set some security options
to ensure your flow editor remains secure from unauthorised access.

It includes a set of default flows that are automatically deployed the first time
Node-RED runs.

### Customising Node-RED

This repository is here to be cloned, modified and re-used to allow anyone create
their own Node-RED based application that can be quickly deployed to IBM Cloud.

The default flows are stored in the `defaults` directory in the file called `flow.json`.
When the application is first started, this flow is copied to the attached Cloudant
instance. When a change is deployed from the editor, the version in cloudant will
be updated - not this file.

The web content you get when you go to the application's URL is stored under the
`public` directory.

Additional nodes can be added to the `package.json` file and all other Node-RED
configuration settings can be set in `bluemix-settings.js`.

If you do clone this repository, make sure you update this `README.md` file to point
the `Deploy to IBM Cloud` button at your repository.

If you want to change the name of the Cloudant instance that gets created, the memory
allocated to the application or other deploy-time options, have a look in `manifest.yml`.

### Environment Variables

The following environment variables can be used to configure the application:

 - `NODE_RED_STORAGE_NAME` - the Cloudant service name as exposed in `VCAP_SERVICES`
 - `NODE_RED_STORAGE_DB_NAME` - the name of the database to use on Cloudant
 - `NODE_RED_STORAGE_APP_NAME` - the prefix used in document names, allowing multiple instances
    to share the same database.
 - `NODE_RED_USERNAME`, `NODE_RED_PASSWORD` - if set, used to secure the editor
 - `NODE_RED_GUEST_ACCESS` - if the editor is secured, this will allow anonymous,
    read-only access
 - `NODE_RED_USE_APPMETRICS` - enables the appmetrics dashboard
