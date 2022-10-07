**Extension Light Shaft :**

![[Pasted image 20221007154343.png]]
Create a plane of a certain size on 4 vertex points (like a portal) to emit a "ray of light" over a certain distance

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


Example file :

v_44_1_daught_deta_ns.ydr

```xml
<Item type="CExtensionDefLightShaft">
     <name>v_44_1_daught_deta_ns</name>
     <offsetPosition x="2.05518913" y="0.704264164" z="0.887825" />
     <cornerA x="2.05518913" y="0.8164527" z="1.044651" />
     <cornerB x="2.05518913" y="0.592075646" z="1.044651" />
     <cornerC x="2.05518913" y="0.592075646" z="0.730999" />
     <cornerD x="2.05518913" y="0.8164527" z="0.730999" />
 ```
 ![[Pasted image 20221007160200.png]]
```xml
<direction x="-0.819751143" y="-0.413016081" z="-0.396769136" />
```
![[Pasted image 20221007154904.png]]
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
