**Extension Light Shaft :**

![image](https://user-images.githubusercontent.com/12967235/194576246-bf5a261a-d215-4a50-9ce6-99f020843322.png)
Create a plane of a certain size on 4 vertex points (like a portal) to emit a "ray of light" over a certain distance in a MLO

Based on [ymap.py from Sollumz](https://github.com/Skylumz/Sollumz/blob/main/cwxml/ymap.py) xml conversion

```python

class ExtensionLightShaft(Extension):

    type = "CExtensionDefLightShaft"

  

    def __init__(self):

        super().__init__()

        self.cornerA = VectorProperty("cornerA")

        self.cornerB = VectorProperty("cornerB")

        self.cornerC = VectorProperty("cornerC")

        self.cornerD = VectorProperty("cornerD")

        self.direction = VectorProperty("direction")

        self.direction_amount = ValueProperty("directionAmount")

        self.length = ValueProperty("length")

        self.fade_in_time_start = ValueProperty("fadeInTimeStart")

        self.fade_in_time_end = ValueProperty("fadeInTimeEnd")

        self.fade_out_time_start = ValueProperty("fadeOutTimeStart")

        self.fade_out_time_end = ValueProperty("fadeOutTimeEnd")

        self.fade_distance_start = ValueProperty("fadeDistanceStart")

        self.fade_distance_end = ValueProperty("fadeDistanceEnd")

        self.color = ValueProperty("color")

        self.intensity = ValueProperty("intensity")

        self.flashiness = ValueProperty("flashiness")

        self.flags = ValueProperty("flags")

        # CExtensionDefLightShaftDensityType

        self.density_type = TextProperty("densityType")

        # CExtensionDefLightShaftVolumeType

        self.volume_type = TextProperty("volumeType")

        self.softness = ValueProperty("softness")

        self.scale_by_sun_intensity = ValueProperty(

            "scaleBySunIntensity", False)

```

Example file I use :
`x64h.rpf\levels\gta5\interiors\v_int_44.rpf\v_44_1_daught_deta_ns.ydr`

Ytyp file used for research (MLO) :
`x64h.rpf\levels\gta5\interiors\v_int_44.rpf\v_int_44.ytyp`
`update\x64\dlcpacks\mpimportexport\dlc.rpf\x64\levels\gta5\interiors\impexp_intwaremed.rpf\imp_impexp_intwaremed.ytyp`

```xml
<Item type="CExtensionDefLightShaft">
     <name>v_44_1_daught_deta_ns</name>
     <offsetPosition x="2.05518913" y="0.704264164" z="0.887825" />
     <cornerA x="2.05518913" y="0.8164527" z="1.044651" />
     <cornerB x="2.05518913" y="0.592075646" z="1.044651" />
     <cornerC x="2.05518913" y="0.592075646" z="0.730999" />
     <cornerD x="2.05518913" y="0.8164527" z="0.730999" />
 ```
 
![image](https://user-images.githubusercontent.com/12967235/194576352-589eabfe-6480-4fff-b019-ac7fd02ea5aa.png)

```xml
<direction x="-0.819751143" y="-0.413016081" z="-0.396769136" />
```

![image](https://user-images.githubusercontent.com/12967235/194576388-6d405edb-e3c0-426c-ba78-218425dc54c6.png)
```xml
     <directionAmount value="1" />
     <length value="2.439765" /> <!-- Length of the shaft in the given direction -->
     <fadeInTimeStart value="0" />
     <fadeInTimeEnd value="0" />
     <fadeOutTimeStart value="0" />
     <fadeOutTimeEnd value="0" />
     <fadeDistanceStart value="0" />
     <fadeDistanceEnd value="0" />
     <color value="0xFFFFB282" />
     <intensity value="50" />
     <flashiness value="0" />
     <flags value="51" /> <!-- tbd -->
     <densityType>LIGHTSHAFT_DENSITYTYPE_QUADRATIC_GRADIENT</densityType>
     <volumeType>LIGHTSHAFT_VOLUMETYPE_SHAFT</volumeType>
     <softness value="0.95" />
     <scaleBySunIntensity value="true" />
    </Item>
```

List of densityType :
- LIGHTSHAFT_DENSITYTYPE_CONSTANT
- LIGHTSHAFT_DENSITYTYPE_SOFT
- LIGHTSHAFT_DENSITYTYPE_SOFT_SHADOW
- LIGHTSHAFT_DENSITYTYPE_SOFT_SHADOW_HD
- LIGHTSHAFT_DENSITYTYPE_LINEAR
- LIGHTSHAFT_DENSITYTYPE_LINEAR_GRADIENT
- LIGHTSHAFT_DENSITYTYPE_QUADRATIC
- LIGHTSHAFT_DENSITYTYPE_QUADRATIC_GRADIENT

List of volumeType :

- LIGHTSHAFT_VOLUMETYPE_SHAFT
- LIGHTSHAFT_VOLUMETYPE_CYLINDER# LightShaft-Research

# Credits

* Dexyfex for [Codewalker](https://github.com/dexyfex/CodeWalker)
* Skylumz for [Sollumz](https://github.com/Skylumz/Sollumz)
* Huge thanks for the first PoC from Sanhje [Website](https://sanhje.net/)
