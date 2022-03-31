# $hit Holes Pothole Tracking API

## Description

## Endpoints

`GET /incidents`
Returns a list of all incidents, by obstruction type and location.

`GET /incidents/<potholeID>`
Returns a list of incidents associated with the specific provided obstruction.

`GET /incidents/<streetName>`
Return a list of incidents which occurred on the provided street.

`GET /incident/<incidentID>`
Return the details of a specific incident.

`POST /incident/`
Report an incident, providing JSON of obstruction, time, and location.


## Resources

## Sample Request
/get/incidents/meadowood --> {street: 'Meadowood Drive', numPotholes: 5, numIncidents: 15, MPIClaimTotal: 25000}
