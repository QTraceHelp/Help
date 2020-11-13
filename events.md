# Events

An Event represents a single step in an Organization's business process for a Product that has been registered in QTrace.  By stringing together a series of Events within a QTrace Session Event, Users are able to define, review, and modify a detailed visual representation of business processes for each Product over time and place.

Events are responsible for setting or changing the status of a Product.

While the information captured at each step in a process may be different depending on the Event type, all Event information is organized based on the same four-dimensional structure (Based on the EPCIS Event standard):

### What
The identifiers of the Products or other objects that are the subject of the Event.

### When
The date, time, and local time zone in effect when an Event took place. 

### Where
The Location at which an Event occurred, and Location where the object(s) are expected to be following the Event.

### Why
Information about the business context, including: an identifier that indicates the business step taking place (e.g., shipping, receiving, etc.), an identifier that indicates the business state of the object(s) following the event (e.g., active, recalled, damaged, etc.), identifiers of the shipping and receiving parties (if the event is part of a process of transfer between parties), links to relevant business transaction documents (e.g., a purchase order, an invoice, etc.), instance- or lot-level master data, and/or other information defined via user extensions.

The following Event Types are supported in QTrace:

- **Commissioning**
    An activity that involves the creation of objects (commissioning of a new object EPC), such as a new trade item lot from a harvest event or a new pallet Serial Shipping Container Code (SSCC).

- **Decommissioning**
Permanently removing objects or products from the system (removal of an object EPC).

- **Receiving**
Objects or products that are received at a location and added to the receiver's inventory.

- **Manufacturing**
    A combination of input objects (products or ingredients) that are transformed into output objects (products).

- **Aggregating**
Objects that are placed into output objects or containers such as boxes of products into pallets of product.

- **Disaggregating**
Removing products (individuals, cases, pallets) from a larger container usually following a Receiving event.

- **Shipping**
Picking goods and packing into containers or onto pallets and transporting.

- **Transporting**
Transporting products or objects from one location to another location.

Any Events that are not used within an organization can be disabled by an Administrator to provide a more streamlined experience for Users. These Events can be reenabled at any time. In addition, custom names can also be entered for Events to keep labels in line with your organization's business process terminology.

An event session is used to capture information related to one or more business processes that involve the creation, movement, or consumption of products over a range of time.