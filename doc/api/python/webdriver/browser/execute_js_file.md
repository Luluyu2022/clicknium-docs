# execute_js_file

***def execute_js_file(
        self,
        locator: Union[_Locator, str], 
        javascript_code: str, 
        method_invoke: str = '', 
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> str***  

Execute javascript file for the target element.

> **Remarks:**
>
>- For javascript script, use "_context$.currentElement." as the target element. 
>- For method invoke, valid method_invoke string should like "run()", or when passing parameters should like "run("execute js", 20)".

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**javascript_file[Required]**: str    
        &emsp;&emsp; javascript file, execute code to target element, use "_context$.currentElement." as the target element, ex: we can set javascript file's content as "function SetText(st){_context$.currentElement.value = st; console.log("execute js"); return \"success\"}"  
    &emsp;**method_invoke**: str    
        &emsp;&emsp; method invoker string, should like "run()", or when passing parameters should like "run("execute js", 20)", ex: for above javascript code, we can set to "SetText(\"execute\")"  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;str, execution result

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # execute js, set text for target element
    # test.js's content can be "function SetText(st){_context$.currentElement.value = st; console.log("execute js"); return \"success\"}"
    result = chrome_browser.execute_js("locator.chrome.cn.search_sb_form_q", "C:\\test\\test.js", "SetText(\"click\")")
```