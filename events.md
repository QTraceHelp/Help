# Events

The basic unit of data in EPCIS is a structure that describes the completion of one business step within an overall business process; this structure is called an EPCIS event. A collection of EPCIS events provides a detailed picture of a business process over time and place.

The information content of a single EPCIS event is organized into four dimensions:[19]

What
The identifiers of the object(s) or other entities that are the subject of the event
When
The date and time when the event took place, and the local time zone in effect
Where
The identifier of the location at which the event occurred, and identifier of the location where the object(s) are expected to be following the event
Why
Information about the business context, including: an identifier that indicates the business step taking place (e.g., shipping, receiving, etc.), an identifier that indicates the business state of the object(s) following the event (e.g., active, recalled, damaged, etc.), identifiers of the shipping and receiving parties (if the event is part of a process of transfer between parties), links to relevant business transaction documents (e.g., a purchase order, an invoice, etc.), instance- or lot-level master data, and/or other information defined via user extensions.
Where the EPCIS data model calls for an identifier, EPCIS allows any URI to be used. Most commonly, the identifiers used are as defined in the EPC Core Business Vocabulary.

Each of the business steps in the process illustrated in the figure could be the source of an EPCIS event. The details of the content of each of those events are different depending on the business step, but all have the same four-dimensional structure.


Simply put, EPCIS 1.1 provides a framework that allows trading partners to know the status of a given trade item or conveyance. EPCIS events affect the status of a trade item or conveyance by changing or setting the object’s disposition (its current state, such as sold, expired, recalled, in transit, or active).


Event Types

EPCIS Events
Electronic Product Code Information Service (EPCIS) Events correspond to the GS1 EPCIS XML message type, and describe trade item observations, transformations, and creation and removal, for both individual and aggregated objects.

The GS1 EPCIS standard is used to codify the event data that members upload to the network. An EPCIS event specifies the What, Where, When, and Why of an event, for one or more trade items.

QTrace supports the following Events:

Commission
Commission Event Data describe the creation of objects (commissioning of a new object EPC), such as a new trade item lot from a harvest event, or a new pallet Serial Shipping Container Code (SSCC).

Each commission event involves one of the following data points:

SSCC
List of class-level trade items (LGTINs) or instance-level trade items (SGTINs) (or both).
Commission events can also contain Instance/Lot Master Data (ILMD).

Decommission
Decommission Event Data describe the deletion of trade items (removal of an object EPC).

Each decommission event involves one of the following data points:

SSCC
List of class-level trade items (LGTINs) or instance-level trade items (SGTINs) (or both).
Observation
Observation Event Data describe trade item observations, such as a product scan at a retailer.

In general, observation events involve one of the following data points, observed at a specific location at a specific time in the course of a business process:

SSCC
List of class-level trade items (LGTINs) or instance-level trade items (SGTINs) (or both).
Transformation
Transformation Event Data describe an irreversible combination of input objects into output objects, such as the creation of chicken breasts from live chicken.

Each transformation event involves both of the following data points:

List of class-level input items (LGTINs) or instance-level input items (SGTINs) (or both)
List of class-level output items (LGTINs) or instance-level output items (SGTINs) (or both).
Transformation events can also contain Instance/Lot Master Data (ILMD).

Aggregation (Agg)
Aggregation Event Data describe a reversible aggregation of input objects into output objects, such as boxes of produce into pallets of produce. Outbound shipping from a supplier to a retailer distribution center is mandated to be an aggregation event.

Each aggregation event involves both of the following data points:

Single parent item (represented, for example, by an SSCC)
List of class-level child items (LGTINs) or instance-level child items (SGTINs) (or both).
Disaggregation (DisAgg)
Disaggregation Event Data describe a disaggregation of objects from a reversible aggregation, such as pallets of produce into boxes of produce.

Each disaggregation event involves both of the following data points:

Single parent item (represented by an SSCC, e.g.)
List of class-level child items (LGTINs) or instance-level child items (SGTINs) (or both).
