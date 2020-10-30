# Events

An Event represents a single step in an Organization's business process for a Product that has been registered in QTrace.  By stringing together a series of Events within a QTrace Session Event, Users are able to define, review, and modify a detailed visual representation of business processes for each Product over time and place.

Events are responsible for setting or changing the status of a Product.

While the information captured at each step in a process may be different depending on the Event type, all Event information is organized based on the same four-dimensional structure (Based on the EPCIS Event standard):

**What** 
The identifiers of the object(s) or other entities that are the subject of the event

**When**
The date and time when the event took place, and the local time zone in effect

**Where**
The identifier of the location at which the event occurred, and identifier of the location where the object(s) are expected to be following the event

**Why**
Information about the business context, including: an identifier that indicates the business step taking place (e.g., shipping, receiving, etc.), an identifier that indicates the business state of the object(s) following the event (e.g., active, recalled, damaged, etc.), identifiers of the shipping and receiving parties (if the event is part of a process of transfer between parties), links to relevant business transaction documents (e.g., a purchase order, an invoice, etc.), instance- or lot-level master data, and/or other information defined via user extensions.


QTrace supports the following Events:

**Commissioning**
Commission Event Data describe the creation of objects (commissioning of a new object EPC), such as a new trade item lot from a harvest event, or a new pallet Serial Shipping Container Code (SSCC).

**Decommissioning**
Decommission Event Data describe the deletion of trade items (removal of an object EPC).

**Receiving**
Observation Event Data describe trade item observations, such as a product scan at a retailer.

**Manufacturing**
Transformation Event Data describe an irreversible combination of input objects into output objects, such as the creation of chicken breasts from live chicken.

**Aggregating**
Aggregation Event Data describe a reversible aggregation of input objects into output objects, such as boxes of produce into pallets of produce. Outbound shipping from a supplier to a retailer distribution center is mandated to be an aggregation event.

**Disaggregating**
Disaggregation Event Data describe a disaggregation of objects from a reversible aggregation, such as pallets of produce into boxes of produce.

**Shipping**
Disaggregation Event Data describe a disaggregation of objects from a reversible aggregation, such as pallets of produce into boxes of produce.

**Transporting**
Disaggregation Event Data describe a disaggregation of objects from a reversible aggregation, such as pallets of produce into boxes of produce.


Any Events that are not used within an Organization can be disabled by an Administrator to provide a more streamlined experience for Users.  If business processes happen to change, these Events can be reenabled at any time.