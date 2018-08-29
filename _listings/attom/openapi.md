swagger: "2.0"
x-collection-name: ATTOM
x-complete: 1
info:
  title: Attom Data Solutions API
  description: attom-empowers-customers-with-better-property-data--we-warehouse-property-data-nationwide-with-myriad-data-points-on-each-parcel-including-ownership-information-latlong-square-footage-loan-types-sales-history-sales-comps-crime-schools-and-more-
  version: 1.0.0
host: search.onboard-apis.com
basePath: /communityapi/v2.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /salestrend/snapshot:
    get:
      summary: Returns sales trends for a given zip code in yearly intervals
      description: Get the average sale price, median sale price, and count of sales
        for the past 2 years in yearly intervals.
      operationId: getSalesTrendByYear
      x-api-path-slug: salestrendsnapshot-get
      parameters:
      - in: header
        name: accept
        description: application/xml or application/json (default)
      - in: header
        name: apikey
        description: Application Key
      - in: query
        name: endmonth
        description: The end month to search from
      - in: query
        name: endyear
        description: The end year to search from
      - in: query
        name: geoid
        description: A list of geographies that this property belongs to
      - in: query
        name: interval
        description: The interval to search from
      - in: query
        name: startmonth
        description: The start month to search from
      - in: query
        name: startyear
        description: The start year to search from
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Sales
      - Trendsa
      - Given
      - Zip
      - Code
      - In
      - Yearly
      - Intervals