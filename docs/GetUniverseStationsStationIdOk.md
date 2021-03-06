
# GetUniverseStationsStationIdOk

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stationId** | **Integer** | station_id integer | 
**name** | **String** | name string | 
**owner** | **Integer** | ID of the corporation that controls this station |  [optional]
**typeId** | **Integer** | type_id integer | 
**raceId** | **Integer** | race_id integer |  [optional]
**position** | [**GetUniverseStationsStationIdPosition**](GetUniverseStationsStationIdPosition.md) |  |  [optional]
**systemId** | **Integer** | The solar system this station is in | 
**reprocessingEfficiency** | **Float** | reprocessing_efficiency number | 
**reprocessingStationsTake** | **Float** | reprocessing_stations_take number | 
**maxDockableShipVolume** | **Float** | max_dockable_ship_volume number | 
**officeRentalCost** | **Float** | office_rental_cost number | 
**services** | [**List&lt;ServicesEnum&gt;**](#List&lt;ServicesEnum&gt;) | services array | 


<a name="List<ServicesEnum>"></a>
## Enum: List&lt;ServicesEnum&gt;
Name | Value
---- | -----
BOUNTY_MISSIONS | &quot;bounty-missions&quot;
ASSASINATION_MISSIONS | &quot;assasination-missions&quot;
COURIER_MISSIONS | &quot;courier-missions&quot;
INTERBUS | &quot;interbus&quot;
REPROCESSING_PLANT | &quot;reprocessing-plant&quot;
REFINERY | &quot;refinery&quot;
MARKET | &quot;market&quot;
BLACK_MARKET | &quot;black-market&quot;
STOCK_EXCHANGE | &quot;stock-exchange&quot;
CLONING | &quot;cloning&quot;
SURGERY | &quot;surgery&quot;
DNA_THERAPY | &quot;dna-therapy&quot;
REPAIR_FACILITIES | &quot;repair-facilities&quot;
FACTORY | &quot;factory&quot;
LABRATORY | &quot;labratory&quot;
GAMBLING | &quot;gambling&quot;
FITTING | &quot;fitting&quot;
PAINTSHOP | &quot;paintshop&quot;
NEWS | &quot;news&quot;
STORAGE | &quot;storage&quot;
INSURANCE | &quot;insurance&quot;
DOCKING | &quot;docking&quot;
OFFICE_RENTAL | &quot;office-rental&quot;
JUMP_CLONE_FACILITY | &quot;jump-clone-facility&quot;
LOYALTY_POINT_STORE | &quot;loyalty-point-store&quot;
NAVY_OFFICES | &quot;navy-offices&quot;
SECURITY_OFFICES | &quot;security-offices&quot;



