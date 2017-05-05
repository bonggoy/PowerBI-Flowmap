## Backgound

Flow maps are a special type of network visualization for object movements, such as the number of people in a migration. A typical flow map, which contains one source and multiple targets, is visualized as a flow-style tree overlaied on top of a map. 

![](assets/screenshot1.png)

The line thicknesses are scaled to represent the values between the source (the root) and the targets (the leaves). By merging edges together, Flow maps can reduce visual clutter and enhance directional trends. 

## Where to Get It

You can get it from the [Office Store](https://store.office.com/zh-cn/app.aspx?assetid=WA104380901&sourcecorrid=ae7baae3-68e1-488c-b34c-ac1e9f8cc8d7&searchapppos=62&ui=zh-CN&rs=zh-CN&ad=CN&appredirect=false) or the [_dist_](https://github.com/weiweicui/PowerBI-Flowmap/tree/master/dist) folder in this repo.

* Update 1.1 (still a draft in the _dist_):
    * add **Advanced - Flow style**: Can change the visualization style between curve, great circle, and straight line.
    * add an optional field **Tooltip**: Now it is customizable. By default, the value field is used.
    * add **Tooltip Format**: Can customize the format of values (if they are numbers) displayed in tooltips.

## How to Use
* Required fields: 
    * **Origin** and **Destination**: These two fields are used to construct relationships. They may be treated as addresses and used to query geo-locations (through [Bing Maps REST Services](https://msdn.microsoft.com/en-us/library/ff701713.aspx)) if latitude/longitude are not specified.
    * **Value**: This field is used to compute flow widths. Negative values will be ignored. 
* Optional fields:
    * **Category**: If specified, the flows that have the same category value will be colored the same.
    * **Origin/Destination latitude/longitude**: These fields specify the geo-locations of sources and targets. 

* Special settings:
    * **Advanced - Flow type**: It can be either `Out-flow`, which constructs flows based on the origins, or `In-flow`, which constructs flows based on the destinations.
    * **Advanced - Flow limit**: This controls the max number of flows that can be displayed simultaneously.


* Need more help? Please leave a comment [here](https://weiweicui.github.io/PowerBI-Flowmap).

***
{% include disqus_comments.html %}
