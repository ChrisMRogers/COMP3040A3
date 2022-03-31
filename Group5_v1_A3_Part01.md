# $hit Holes Pothole Tracking API

## Description
$hit Holes is designed to give drivers and Manitoban citizens information about the quality of our roads. Every year Manitobans pay tens of thousands of dollars repairing their vehicles because of the general lack of upkeep of our public roads, to combat this, $hit Holes will inform drivers of which streets to avoid. In the unfortunate event of a crash related to road infrastructure, $hit Holes will bolster your claim with MPI by telling you how many other drivers have also experienced an incident on this road. By allowing users the ability to upload and update the roads they drive on every day, our data will always remain as fresh as possible.
## Endpoints

`GET /potholes`
Returns a list of all potholes by location.

`GET /incidents`
Returns a list of all incidents, by obstruction type and location.

`GET /incident/<potholeID>`
Returns the most recent incident associated with the specific provided obstruction.

`GET /incident/<streetName>`
Return the most recent incident which occurred on the provided street.

`GET /incidents/<potholeID>`
Returns a list of incidents associated with the specific provided obstruction.

`GET /incidents/<streetName>`
Return a list of incidents which occurred on the provided street.

`GET /incident/<incidentID>`
Return the details of a specific incident.

`GET /potholes/<street>`
Returns a list of potholes which are located on a specific street.

`GET /potholes/<incident>`
Returns a list of potholes which are involved in a specific incident.

`GET /pothole/<potholeID>`
Returns the details of a specific pothole.

`POST /incident/`
Report an incident, providing JSON of obstruction, time, and location.

`POST /pothole/`
Report an pothole, providing JSON of pothole location.

`PUT /incident/`
Update a reported incident, providing JSON of obstruction, time, and location.

`PUT /pothole/`
Update a reported pothole, providing JSON of pothole location.

## Resources

A JSON list of incidents caused by bad road infrastructure.

## Sample Request
/get/incidents/meadowood --> {street: 'Meadowood Drive', numPotholes: 5, numIncidents: 15, MPIClaimTotal: 25000}
