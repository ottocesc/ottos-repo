<![endif]-->

SDD – Properties- BOM item – SCON-4121![enter image description here](https://github.com/ottocesc/ottocesc.github.io/blob/master/assets/variantconfig.PNG)
![enter image description here](ottocesc.github.io/assets/variantconfig.PNG)

Requirements

In the Inspector ‘s properties should be set for the BOM based calls

The task

Implement the properties tab in the inspector component.

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)<![endif]>

**_UI API function._**

The inspector component is under the i2d.lo.lib.vchclf project. API call to load the inspector ‘s bom item properties is:  
<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)<![endif]>

Note: _sBOMNodePath_ should be of entity type BOMNode and through ConfiguraitonContext navigation property**.  
Sample path: _/ConfigurationContextSet(ContextId=CONTEXT_ID)/BOMNodes('1_1')_**

**_UI related controllers and views_**

_BOMBased:_ which handles the main functionality for the main layout.  
_BOMItemProperties_: contains the specific implementation/ definition for the properties

**_Entity._**

**The BOM item based calls are bound to the _BOMNodes_ entity Set and it is under the LO_VCHCLF gateway project. it contains the following properties.  
**<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image005.jpg)<![endif]>**  
  
And It also uses the ConfigurationContext entity type to get related information regarding the BOM. it contains the following properties:**

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image007.jpg)<![endif]>**  
  
NOTE: in the Simulation environment, the ObjectKey is the simulation id.**

**_BACKEND._**

**The implementation could be found under the _ODATA_LO_VCHCLF_COMMON_ package under the _CL_LO_VCHCLF_DPC_EXT_ class. The get entity and get entity set functionalities are implemented using the redefined function: _BOMNODESET_GET_ENTITYSET and BOMNODESET_GET_ENTITY_.**

**The test class is _: ltc_bomnodeset_**  **which used the _ltd_runtime_bom_ test double to mock the runtime object.  
  
The retrieval functionality is implemented under the _CL_LO_VCHCLF_VCH_RT_ class in the _ODATA_LO_VCHCLF_VCH_ package. _GET_BOM_NODE_ function is used to retrieve the related properties.  for more in-depth information regarding this please check the BOM explosion SDD**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1NTc2MzM5NzEsLTUyOTA5OTQwMCw3OD
AwOTI5ODhdfQ==
-->