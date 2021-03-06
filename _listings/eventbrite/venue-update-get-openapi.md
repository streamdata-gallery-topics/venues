---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get Venue Update
  description: This method updates an existing venue. Only the fields passed as arguments
    will be modified. It returns the ID of the updated venue.
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{id}/venues/:
    get:
      summary: Get Users Venues
      description: Returns a paginated response of venue objects that are owned by
        the user.
      operationId: getUsersVenues
      x-api-path-slug: usersidvenues-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - Venues
  /organizations/{id}/venues/:
    post:
      summary: Post Organizations Venues
      description: Creates new venue objects under an organization and returns it
        as venue.
      operationId: postOrganizationsVenues
      x-api-path-slug: organizationsidvenues-post
      parameters:
      - in: query
        name: venue.address.address_1
        description: The first line of the address
        type: query
      - in: query
        name: venue.address.address_2
        description: The second line of the address
        type: query
      - in: query
        name: venue.address.city
        description: The city where the venue is
        type: query
      - in: query
        name: venue.address.country
        description: The country where the venue is
        type: query
      - in: query
        name: venue.address.latitude
        description: The latitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.longitude
        description: The longitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.postal_code
        description: The postal_code where the venue is
        type: query
      - in: query
        name: venue.address.region
        description: The region where the venue is
        type: query
      - in: query
        name: venue.age_restriction
        description: The age restrictions for the venue
        type: query
      - in: query
        name: venue.capacity
        description: The max capacity for the venue
        type: query
      - in: query
        name: venue.google_place_id
        description: The google place id for the venue
        type: query
      - in: query
        name: venue.name
        description: The name of the venue
        type: query
      - in: query
        name: venue.organizer_id
        description: The organizer this venue belongs to (optional - leave this off
          to use the default organizer)
        type: query
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Venues
  /venues/{id}/:
    get:
      summary: Get Venues
      description: Returns a venue object.
      operationId: getVenues
      x-api-path-slug: venuesid-get
      responses:
        200:
          description: OK
      tags:
      - Venues
    post:
      summary: Post Venues
      description: Updates a venue and returns it as an object.
      operationId: postVenues
      x-api-path-slug: venuesid-post
      parameters:
      - in: query
        name: venue.address.address_1
        description: The first line of the address
        type: query
      - in: query
        name: venue.address.address_2
        description: The second line of the address
        type: query
      - in: query
        name: venue.address.city
        description: The city where the venue is
        type: query
      - in: query
        name: venue.address.country
        description: The country where the venue is
        type: query
      - in: query
        name: venue.address.latitude
        description: The latitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.longitude
        description: The longitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.postal_code
        description: The postal_code where the venue is
        type: query
      - in: query
        name: venue.address.region
        description: The region where the venue is
        type: query
      - in: query
        name: venue.age_restriction
        description: The age restrictions for the venue
        type: query
      - in: query
        name: venue.capacity
        description: The max capacity for the venue
        type: query
      - in: query
        name: venue.google_place_id
        description: The google place id for the venue
        type: query
      - in: query
        name: venue.name
        description: The name of the venue
        type: query
      - in: query
        name: venue.organizer_id
        description: The organizer this venue belongs to (optional - leave this off
          to use the default organizer)
        type: query
      responses:
        200:
          description: OK
      tags:
      - Venues
  /venues/:
    post:
      summary: Post Venues
      description: Creates a new venue with associated address.
      operationId: postVenues
      x-api-path-slug: venues-post
      parameters:
      - in: query
        name: venue.address.address_1
        description: The first line of the address
        type: query
      - in: query
        name: venue.address.address_2
        description: The second line of the address
        type: query
      - in: query
        name: venue.address.city
        description: The city where the venue is
        type: query
      - in: query
        name: venue.address.country
        description: The country where the venue is
        type: query
      - in: query
        name: venue.address.latitude
        description: The latitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.longitude
        description: The longitude of the coordinates for the venue
        type: query
      - in: query
        name: venue.address.postal_code
        description: The postal_code where the venue is
        type: query
      - in: query
        name: venue.address.region
        description: The region where the venue is
        type: query
      - in: query
        name: venue.age_restriction
        description: The age restrictions for the venue
        type: query
      - in: query
        name: venue.capacity
        description: The max capacity for the venue
        type: query
      - in: query
        name: venue.google_place_id
        description: The google place id for the venue
        type: query
      - in: query
        name: venue.name
        description: The name of the venue
        type: query
      - in: query
        name: venue.organizer_id
        description: The organizer this venue belongs to (optional - leave this off
          to use the default organizer)
        type: query
      responses:
        200:
          description: OK
      tags:
      - Venues
  /venues/{id}/events/:
    get:
      summary: Get Venues Events
      description: Returns events of a given venue.
      operationId: getVenuesEvents
      x-api-path-slug: venuesidevents-get
      parameters:
      - in: query
        name: only_public
        description: Only show public events even if viewing your own events
        type: query
      - in: query
        name: order_by
        description: 'How to order the results (Valid choices are: start_asc, start_desc,
          created_asc, or created_desc)'
        type: query
      - in: query
        name: start_date.range_end
        description: Only return events with start dates before the given date
        type: query
      - in: query
        name: start_date.range_start
        description: Only return events with start dates after the given date
        type: query
      - in: query
        name: status
        description: Only return events with a specific status set
        type: query
      responses:
        200:
          description: OK
      tags:
      - Venues
      - Events
  /user_list_venues:
    get:
      summary: Get User List Venues
      description: This method lists the venues created by this user. Requires authentication.
      operationId: Get_user_list_venues_
      x-api-path-slug: user-list-venues-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      responses:
        200:
          description: OK
      tags:
      - User
      - List
      - Venues
  /venue_get:
    get:
      summary: Get Venue Get
      description: This method returns a single venue by id.
      operationId: Get_venue_get_
      x-api-path-slug: venue-get-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: id
        description: The venue id
      responses:
        200:
          description: OK
      tags:
      - Venue
      - Get
  /venue_new:
    get:
      summary: Get Venue New
      description: This method creates a new venue. It returns the ID of the newly
        created venue.
      operationId: Get_venue_new_
      x-api-path-slug: venue-new-get
      parameters:
      - in: query
        name: adress
        description: The venue address (line 1)
      - in: query
        name: adress_2
        description: The venue address (line 2)
      - in: query
        name: city
        description: The venue city
      - in: query
        name: country_code
        description: 2-letter country code, according to the ISO 3166 format
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: organizer_id
        description: The ID of the related organizer
      - in: query
        name: postal_code
        description: The postal code of the venue
      - in: query
        name: region
        description: The venue state/province/county/territory depending on the country
      - in: query
        name: venue
        description: The venue name
      responses:
        200:
          description: OK
      tags:
      - Venue
      - New
  /venue_update:
    get:
      summary: Get Venue Update
      description: This method updates an existing venue. Only the fields passed as
        arguments will be modified. It returns the ID of the updated venue.
      operationId: Get_venue_update_
      x-api-path-slug: venue-update-get
      parameters:
      - in: query
        name: adress
        description: The venue address (line 1)
      - in: query
        name: adress_2
        description: The venue address (line 2)
      - in: query
        name: city
        description: The venue city
      - in: query
        name: country_code
        description: 2-letter country code, according to the ISO 3166 format
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: id
        description: The venue ID
      - in: query
        name: postal_code
        description: The postal code of the venue
      - in: query
        name: region
        description: The venue state/province/county/territory depending on the country
      - in: query
        name: venue
        description: The venue name
      responses:
        200:
          description: OK
      tags:
      - Venue
      - Update
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---