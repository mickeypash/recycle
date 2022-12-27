# ♻️ Recycling list app ♻️

### Goals:
 - Learn a bit more about recycling
 - Specifically how it's done in my current [London Borough](https://www.towerhamlets.gov.uk/Home.aspx)
 - Get an awarenes of the mobile dev space (Native vs Cross Platform)
 - Learn a bit about Flutter
 - Learn [How to write a Software Design Document](https://mickeys.link/e64fdc)
 - Practice design thinking

Recycling is every **Wednesday** 
General waste is every **Tue** and **Friday**


### How can I distil cumbersome textual information from council site?

I'll start with a simple use-case. Look at the borough of Tower Hamlet's website. I would say it exceeds my expectations. However I think we could do better. A simple clear list with only the essential information would be better. 

To constrain myself further I've selected a few items that I often wonder what to do with:
- Plastic bags
    * Some supermarkets collect plastic bags for recycling
    * Reduce plastic bag waste by taking reusable bags shopping.
- Shoes
    * drop them off at a local charity shop
    * recycle them through a network of special textile and shoe recycling bins throughout the borough
- Cartons
- Plastic containers
    * yogurt pots
    * plastic drink bottles
    * cleaning product bottles
    * toiletry bottles
    * plastic flower pots
    * margarine containers
    * ice cream tubs
    * fruit punnets

I'm so ADHD these days I just needed something as simple as table.
If I extract it into a static page I can have a nice little short link which can tell me whether something is recyclable. E.g. `toiletry bottles` and `margarine containers` are some things I never really recycle and didn't know that if I rinse them I can.

| Product                  |  Rinse |
|:-------------------------|:------:|
| plastic drink bottles    |   ✅   |
| yogurt pots              |   ✅   |
| cleaning product bottles |   ✅   |
| toiletry bottles         |   ✅   |
| plastic flower pots      |   ✅   |
| margarine containers     |   ✅   |
| ice cream tubs           |   ✅   |
| fruit punnets            |   ✅   |
| cartons                  |   ✅   |


Link to [Tower Hamlets API Endpoint](http://ratings.food.gov.uk/OpenDataFiles/FHRS530en-GB.json)
Current schema:
```json
{
  "FHRSEstablishment": {
    "Header": {
      "ExtractDate": "2020-07-22",
      "ItemCount": "2598",
      "ReturnCode": "Success"
    },
    "EstablishmentCollection": {
      "EstablishmentDetail": [
        {
          "FHRSID": "1227622",
          "LocalAuthorityBusinessID": "202990",
          "BusinessName": "1947 Restaurant & Bar",
          "BusinessType": "Takeaway/sandwich shop",
          "BusinessTypeID": "7844",
          "AddressLine2": "38 Middlesex Street",
          "AddressLine3": "London",
          "PostCode": "E1 7EX",
          "RatingValue": "4",
          "RatingKey": "fhrs_4_en-GB",
          "RatingDate": "2020-02-26",
          "LocalAuthorityCode": "530",
          "LocalAuthorityName": "Tower Hamlets",
          "LocalAuthorityWebSite": "http://www.towerhamlets.gov.uk",
          "LocalAuthorityEmailAddress": "foodsafety@towerhamlets.gov.uk",
          "Scores": {
            "Hygiene": "5",
            "Structural": "0",
            "ConfidenceInManagement": "10"
          },
          "SchemeType": "FHRS",
          "NewRatingPending": "False",
          "Geocode": {
            "Longitude": "-0.07550500000000",
            "Latitude": "51.51582500000000"
          }
```

### References
- https://www.towerhamlets.gov.uk/lgnl/environment_and_waste/recycling_and_waste/a-z_recycling_guide.aspx#
- https://forms.towerhamlets.gov.uk/service/Check_your_waste_and_recycling_collection_days
- https://recyclecoach.com/residents/recyclepedia/
- https://recyclenation.com/
- https://lewisham.gov.uk/myservices/wasterecycle
- https://www.recycleyourelectricals.org.uk/
