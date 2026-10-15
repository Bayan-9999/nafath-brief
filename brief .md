Version: NAFATH-V2 
Track:  Networking 

Overview
The emergency-response system uses six main IT areas that work together. Software should manage failed requests and avoid performing the same action twice when a request is sent again. AI can predict network traffic problems and should give good results in different situations. Mobile apps must work without internet and update their data when the connection returns. Networking uses 5G slicing to provide suitable speed, response time, and connection quality. Cybersecurity helps identify attacks, control risks, and recover services. Data modeling organizes information into simple daily and regional reports. Together, these areas help maintain reliable services during network problems and cyberattacks. availability, accurate decisions and operational continuity during congestion, outages and cyberattacks. For the Networking track, the key topic is how 5G network slicing could provide dedicated service characteristics for emergency responders.

Software
Safe HTTP methods include GET, HEAD, OPTIONS, and TRACE because they do not change data on the server. Also these methods are idempotent. PUT and DELETE are idempotent, meaning repeating the request has the same result as sending it once, but they are not safe. POST and PATCH are not always idempotent. Therefore, retrying safe or idempotent requests is usually reliable, while repeating POST requests may create duplicate records or actions.

Resource: RFC 9110 - HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110.html 
AI
Overfitting happens when a congestion model learns too much from its training data, including noise, and makes poor predictions on unseen conditions. Cross-validation helps check the model by splitting historical network data into several training and testing groups. The results from these groups show how well the model works in different situations. A large difference between training and validation performance, or unstable results between folds, can reveal overfitting before deployment. 

Resource: Cross-validation: evaluating estimator performance - https://scikit-learn.org/stable/modules/cross_validation.html 
Mobile
The responder app should be designed to work without an internet connection. It should show saved information, keep important features working, and store new reports or updates until the connection returns. Each saved change should have a unique ID, timestamp, and sync status. When the connection returns, the app should send pending updates and receive new data. Clear rules should prevent important or newer information from being replaced by older data.

Resource: Build an offline-first app - https://developer.android.com/topic/architecture/data-layer/offline-first

Networking

Cybersecurity

Data

Misconception in My Track

Open Question
