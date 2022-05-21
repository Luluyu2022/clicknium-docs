# clicknium.wait_appear
***def wait_appear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> UiElement***  

Wait for the element appear.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, or None if the element is not appear


**Example:**
***
```python
from clicknium import clicknium as cc, locator

#wait element appear
cc.wait_appear(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.wait_appear(locator.notepad.notepad.document_151, variables)
```