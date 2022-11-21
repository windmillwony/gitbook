# Junction Builder

Junction Builder is a product designed to implement **multi child records handling** without coding.

<figure><img src="../../.gitbook/assets/Junction builder.png" alt=""><figcaption><p>Junction bulider</p></figcaption></figure>

Quoting is a typical multi child records processing task in Salesforce.com

{% hint style="info" %}
A quotation job consists of 1) the quotation object, which is **the parent** that contains information such as the customer, payment terms, and expiration date, and 2) the quotation line item object, which is **the child**, which contains the quantity, selling price, and discount rate for each product.

At this time, the child object is also a Junction object that looks up the price list object that stores price information and product information.

Typically, when quoting, you are quoting for one or more products. Since multiple products are selected and the quantity and price are entered on one screen, a multi record processing function is required.
{% endhint %}

<figure><img src="../../.gitbook/assets/Quote Object Relationship.png" alt=""><figcaption><p>Quote Object Relationship</p></figcaption></figure>

{% hint style="info" %}
Of course, quoting is one of the main features that Salesforce offers out of the box. However, in many cases, custom development is necessary when there are special company-specific requirements, for example when inventory and linkages are required or prices in a multi dimensional structure are to be displayed.
{% endhint %}

Not only Quote, also many business operations require multi child records processing capabilities. For example, an order action that has multiple order items as children is another typical example.

**More cases where we can use Junction builder.**

| Case                                                                                            | Parent Object | Child Object           | Lookup Object         |
| ----------------------------------------------------------------------------------------------- | ------------- | ---------------------- | --------------------- |
| Register Sample Request from Opportunity (Select Multi Child Records from Opportunity Products) | Opportunity   | Sample Request Product | Opportunity Line Item |
| Register revenue schedule from opportunity                                                      | Opportunity   | Sales Schedule         | Opportunity Line Item |
| Register required parts from work order                                                         | Work Order    | Required parts         | Product               |
| Business trip planning (visiting multiple destinations)                                         | BizTrip\_\_c  | Destination\_\_c       | Account               |
