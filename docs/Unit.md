

# Unit


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**name** | **String** |  |  [optional] |
|**unitNumber** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**price** | **BigDecimal** |  |  [optional] |
|**bed** | **BigDecimal** |  |  [optional] |
|**bath** | **BigDecimal** |  |  [optional] |
|**sqft** | **BigDecimal** |  |  [optional] |
|**model** | **String** |  |  [optional] |
|**floor** | **String** |  |  [optional] |
|**orientation** | **String** |  |  [optional] |
|**parking** | **BigDecimal** |  |  [optional] |
|**unitmodels** | [**List&lt;UnitModel&gt;**](UnitModel.md) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| AVAILABLE | &quot;Available&quot; |
| ON_HOLD | &quot;OnHold&quot; |
| SOLD | &quot;Sold&quot; |
| LEASED | &quot;Leased&quot; |
| UNAVAILABLE | &quot;Unavailable&quot; |



