[service-omnichannel](../../../../README.md) / [API](../README.md) / [Analyses](./README.md) / get analyse data 

# Get client anlayse data

Get analyse data  of client . 

```text
GET analyses/:id/data
```

## Body

| Name           | Description                                         |
|----------------|-----------------------------------------------------|
| `user`         | The client's user information                       |
| `workspaceId`  | The current workspaceId                             |


## Parameters

| Name           | Description                                         |
|----------------|-----------------------------------------------------|
| `id`           | analyse id                                          |



## Example

```text
GET analyses/665746252624a663d285deb0/data

{
  "user": {
    "id": "123-abc-456",
    "workspaces": ["fake-id24"]
  },
  "workspaceId": "fake-id24"
}
```

Response

```text
200
```

```json

{
  "analyseId": "667973e4b4233ee15adb76d5",
  "analyseName": "Test analyse name",
  "conversionsPaths": [
    {
      "path": [
        "Organic Search",
        "Organic Search",
        "Organic Search",
        "Organic Search",
        "Organic Search",
        "Organic Search"
      ],
      "nb_touchpoints": 6,
      "conversions": 75,
      "conversionValues": 206257.82831
    },
    {
      "path": [
        "Email"
      ],
      "nb_touchpoints": 1,
      "conversions": 74,
      "conversionValues": 192519.426396
    },
    {
      "path": [
        "Paid Search",
        "Paid Search"
      ],
      "nb_touchpoints": 2,
      "conversions": 64,
      "conversionValues": 143773.994764
    }
  ],
  "channelsAttribution": [
    {
      "channelName": "Paid Other",
      "Model": "markov",
      "conversions": "2",
      "conversionValues": "869"
    },
    {
      "channelName": "Paid Other",
      "Model": "markov",
      "conversions": "1",
      "conversionValues": "933"
    }
   ],
  "channelsSummaries": [
    {
      "channelName": "Organic Video",
      "initiatorConversions": 93,
      "assistantConversions": 170,
      "finisherConversions": 37,
      "autonomousConversions": 95,
    },
    {
      "channelName": "Organic Social",
      "initiatorConversions": 14,
      "assistantConversions": 29,
      "finisherConversions": 5,
      "autonomousConversions": 13,
    } 
  ],
  "channelsPresence": [
    {
      "channelName": "Paid Search",
      "presenceConversions": 2513
    },
    {
      "channelName": "Organic Search",
      "presenceConversions": 2896
    }
  ],
  "nbPaths": 2085,
  "turnover": 19808120.11594794,
  "mono": 2412,
  "multi": 5455,
  "conversions": 7867    

}    
            

```