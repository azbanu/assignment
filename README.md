<strong>Offer Management Rest Service</strong></br></br>
This web service allows offer to be managed via REST 

<strong>Technology Stack</strong></br></br>
Spring Boot</br>
Embeded H2 </br>
Spring MVC Framework</br>
Maven</br>
Jersey</br>
Mockito</br>

<strong>Assumptions</strong></br></br>
Expiry date is in ISO Date Time format (2019-03-25T00:00:00.000) </br>
All domain fields are mandatory </br>
No i18n support </br>
Schedule will run every 10 seconds without impacting performance.   </br> 
Offers that expire in between scheduler run will be captured and set at service layer but will not be saved until the next scheduler run </br>
format in JSON </br>

<strong>End points</strong></br></br>
Service entry point  at http://localhost:8080/api/offer </br></br>
Request to list all offers: GET  http://localhost:8080/api/offer/list </br>
Response with all available offers </br></br>
 
Request to list offers with given description: GET http://localhost:8080/api/offer/list/?description=description </br>
Response with all offers matching description</br></br>
 
Request to add offer: POST http://localhost:8080/api/offer/ using JSON payload </br>
Respond with the created offer </br>
{
   "name": "offer",
   "description": "offer description",
   "price": "2",
   "currency": "GBP",
   "expiryDate": "2019-03-04T20:49:02.231"
 }
</br></br>
  
Request to cancel offer: PUT http://localhost:8080/api/offer/cancel/{id} </br>
Response with the cancelled offer </br></br>
  
Request to get offer by id: GET http://localhost:8080/api/offer/{id} </br>
Response with the offer</br></br>

<strong>Build and Run</strong></br></br>

