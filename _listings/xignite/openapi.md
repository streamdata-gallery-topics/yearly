swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite VWAP
  description: provides-delayed-and-historical-volumeweightedaverage-price-vwap-information-
  version: 1.0.0
host: www.xignite.com
basePath: xVWAP.json/XigniteVWAP
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetYearlyHighLowPrice:
    get:
      summary: Get Yearly High Low Price
      description: Returns yearly high, low prices for a specific bond reported by
        the price source selected in the input. Request against this operation counts
        as one hit.
      operationId: GetYearlyHighLowPrice
      x-api-path-slug: getyearlyhighlowprice-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Yearly
      - High
      - Low
      - Price
  /GetYearlyHighLowPrices:
    get:
      summary: Get Yearly High Low Prices
      description: Returns yearly high, low prices for the list of bonds specified
        in the input, as reported by the price source selected in the input. Each
        YearlyHighLowPrice object returned counts as one hit.
      operationId: GetYearlyHighLowPrices
      x-api-path-slug: getyearlyhighlowprices-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Yearly
      - High
      - Low
      - Prices