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
5G network slicing creates separate logical networks with different capabilities using the same physical infrastructure. A special slice for emergency services can provide enough capacity, low delay, reliable connections, and better security for calls, location, video, and incident reports. During busy periods, network rules can give emergency teams priority over regular network traffic . However, reliable service also needs good network coverage, enough system capacity, backup power, and regular monitoring.

Resource: 5G Network slice management - https://www.3gpp.org/technologies/slice-management 

Cybersecurity
The cybersecurity process starts with preparation, including setting rules, identifying important systems, and applying security controls. Detection helps find unusual activity and confirm attacks. During response, the team checks the damage, limits the problem by isolating affected systems, and removes threats. Recovery restores safe services, checks that they work properly, and increases monitoring. Finally, the team reviews what happened and uses the lessons to improve security plans, controls, training, and future decisions.

Resource: NIST SP 800-61 Rev. 3 - Incident Response Recommendations and Considerations for Cybersecurity Risk Management - https://csrc.nist.gov/pubs/sp/800/61/r3/final
Data
A star schema uses a central table for usage data, linked directly to tables such as date, region, service, and responder organization. A snowflake schema splits these tables into smaller related tables, which reduces repeated data but makes queries more complex. For daily usage reports by region, a star schema is a better choice because it is easier to understand, simplifies data calculations, and supports faster analysis.

Resource: Understand star schema and the importance for Power BI - https://learn.microsoft.com/en-us/power-bi/guidance/star-schema
Misconception in My Track
A common misunderstanding is that a dedicated 5G network slice is a fully separate physical network that always keeps emergency communications working. In fact, a slice is a logical network that uses shared infrastructure to provide specific services and features. Its reliability depends on proper resource management, service requirements, regular monitoring, and security. It also depends on the strength and reliability of the main radio and core networks.

Open Question
I would check the required service levels, reserved network capacity, and backup systems to keep the emergency-response network slice working during heavy traffic, network site outages, or failures in shared core systems.
