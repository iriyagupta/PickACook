# PickACook
The repository to keep track of the progress within the codebase of the application. 

This project aims to create an app for Pick A Cook which is an on-demand booking platform for booking private chefs. The app shall work for both private chefs and customers. Therefore, it will be able to swtich between two interfaces depending on the user type.

## Customer Interface

### Steps
<ol>
  <li>Registration</li>
    <ol>
      <li>Last Name </li>
      <li>First Name</li>
      <li>E-Mail</li>
      <li>Phone no.</li>
    </ol>
  <li>Entering the request
    <ol>
      <li>Location</li>
      <li>Date</li>
      <li>Number of guests</li>
      <li>Cuisine</li>        
    </ol>
  </li>
  <li>Matching algorithm runs</li>
  <li>Search results</li>
  <li>Filter results</li>
  <li>Choose chef</li>
  <li>Send booking request</li>
</ol>

### Questions and Comments
<p>Registration Interface: Will be skipped as long as the user is logged in.</p>
<p>Location: What is the administration level (ZIP-Code, district, municipality, city)? What information do we collect? Collecting only high level data is more time efficient. In the end, it is up to the chosen cook to decide whether or not to confirm the booking request.To be explicit, location does not refer to the chef's restaurant workplace or residence location but covers the chef's (preferred) area of work</p>
<p>Date: The date only is not precise enough. We need the time as well. Maybe an interface similar to Doodle's time slots? We should include an option "open-end" or "overnight".</p>
<p>Cuisine: We probably need a hierarchical (nested?) structure: All &#8594; Western | Asian | African | Latin-American &#8594; Taking Asian for example then Korean | Chinese | Indian | etc.;<br>Optionally, we might as well think about including categories such as "Mediterranean" or "South-East-Asian"<br>We shouldn't forget about categories like "Vegeterian", "Vegan", "Fusion", "High-end", "comfort food". Maybe provide these categories as clickable tags for both customer and chef from a list</p>
<p>Matching and results: Matching algorithm implies that we already have a rich data and some kind of structured data bank on our backend side. Does anyone have experience with SQL or similar? Can we create a dummy data bank to test our program? Assuming that the search results will show an ordered "best matches" list, the question arises how the ranking calculation is performed. In terms of prioritization of search inputs, date and time is probably the most important. For residual parameteres location and cuisine, the proximity between the user's location and the chef's preferred area of work can be used to score the "matchability" with respect to location. With respect to cuisine, if user wishes "Thai" cuisine which is unfortunately not available for the date and time and location, other South-East-Asian cuisines will rank highest, followed by the rest of the country-level cuisines under the "Asian" category. Essentially, the search for the best match cuisine will crawl through the neighborhood of the cuisine term specified by the suser if the cuisine term is not immediately found. If the specified cuisine term has no descendents, then all the children of its parent cuisine term, i.e. the specified cuisine term's siblings, will be ranked highest, but equally. If the specified cuisine term has descendants, similary as before, all its children will be ranked highest and equally.</p>
<p>Filtering categories<ul>
  <li>Usual price per person: Assuming no extra options have been booked (e.g. cutlery, beverages, maybe some kind of entertainment package)</li>
  <li>Review</li>
  <li>No. of Bookings</li>
  <li>Entertainment package</li>
  <li>Language</li>
  </ul>
</p>
<p>Booking request: Chef should answer within 24 hours. If not, we try to contact the chef. Should we allow for several simultaneous booking requests? We should show the an icon with the number of pending request and as soon as a request has been confirmed (by the chef and/or us), the remaining pending requests will be automatically cancelled.

## Chef Interface
After creating an account on our app, we will send the chef a message with an introduction to a screening process (who does that? maybe an external identity validation company like for when you open an online bank account or register on bumble lol?). During the registration process the chef must meet certain requirements in order to be accepted. If the requirements are met, a message will be sent to him. In case of refusal, the reason will be explained and how it can be accepted when reapplying. After successfully completing the screening process, he will receive a welcome package and his account will be opened.
As a chef he will have the possibility to enter his availability at the beginning of the month. This availability must be detected in the system so that the customer can reserve this date with the cook. When a booking is made, the chef will be informed and the booking is then binding. 

The key screens will be 1. the booking screen for the customer in which the customer can choose the preferred kitchen and chef. The 2. key screen will be an overview screen with all bookings for the chef. The screen should show a summary of all bookings with him.

Features: (See "Questions and Comments")
1. Matching (map): We will need a smart matching process that can recommend certain chefs around an area to the selection of the customer.
2. Booking system: The customer must be able to reserve a slot of the available slots of the chef. The slot must be blocked (and unblocked in case of cancellation). 
3. 


Operating systems:
Android
IOS

Installation Packages:
.....
