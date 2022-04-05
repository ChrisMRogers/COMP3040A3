# $hit Holes Pothole Tracking API

## Description
$hit Holes is designed to give drivers and Manitoban citizens information about the quality of our roads. Every year Manitobans pay tens of thousands of dollars repairing their vehicles because of the general lack of upkeep of our public roads, to combat this, $hit Holes will inform drivers of which streets to avoid. In the unfortunate event of a crash related to road infrastructure, $hit Holes will bolster your claim with MPI by telling you how many other drivers have also experienced an incident on this road. By allowing users the ability to upload and update the roads they drive on every day, our data will always remain as fresh as possible.

## Endpoints

`GET /potholes`
Returns the details of potholes within Manitoba.

### Endpoint Parameters

- `location - location string to narrow search results` 
- `minNumIncidents - minimum number of required related incidents`
- `minMPIClaimTotal - minimum total claimed through MPI`

## Resources

```
GET /potholes?location=streetLocation&minNumIncidents=numMinIncidents&minMPIClaimTotal=minTotal 
```
**Responds**
```
{
	"potholeID": ID,
	"numIncidents": 0,
	"MPIClaimTotal": 0,
	"street": ''
}
```

## Sample Request
The query can be made with no parameters which will return all potholes in Manitoba
```
GET /potholes
```
**Responds**
```
[
  {
		"potholeID": 5424,
		"numIncidents": 15,
		"MPIClaimTotal": 6000,
		"street": "Machray Ave"
	},
	{
		"potholeID": 4325,
		"numIncidents": 5,
		"MPIClaimTotal": 24500,
		"street": "Church Ave"
	},
        ...
        ...
        ...
	{
		"potholeID": 4326,
		"numIncidents": 1,
		"MPIClaimTotal": 4500,
		"street": "Parr St"
	}
]
```


Or parameters can be supplied in order to narrow down the returned results

```
GET /potholes?location='Meadowood'&minNumIncidents=10&minMPIClaimTotal=15000
```
**Responds**
```
[
  {
		"potholeID": 3423,
		"numIncidents": 11,
		"MPIClaimTotal": 16000,
		"street": "Meadowood Drive"
	},
	{
		"potholeID": 4321,
		"numIncidents": 13,
		"MPIClaimTotal": 15500,
		"street": "Wales Ave"
	},
	{
		"potholeID": 3214,
		"numIncidents": 12,
		"MPIClaimTotal": 27000,
		"street": "Pembridge Bay"
	}
]
```
