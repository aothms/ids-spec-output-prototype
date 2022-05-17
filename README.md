## Non-existent entity name

~~~xml
<entity>
  <name>
    <simpleValue>IfcRabbit</simpleValue>
  </name>
</entity>
~~~

[fail_non-existent_entity_name.ids](c.ids_filename)

~~~lua
#21=IfcWall('0ygfJG68L7fhTfY31eSv7O',$,$,$,$,$,$,$,$)
~~~

[fail_non-existent_entity_name.ifc](c.ifc_filename)

Expected result: fail

## Entity matching

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[pass_entity_matching.ids](c.ids_filename)

~~~lua
#21=IfcWall('1oIAy1SoXFV8qIqUQNRhiS',$,$,$,$,$,$,$,$)
~~~

[pass_entity_matching.ifc](c.ifc_filename)

Expected result: pass

## Entity with PredefinedType

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[pass_entity_with_predefinedtype.ids](c.ids_filename)

~~~lua
#21=IfcWall('3b$A_Y4HzCQOTGJ7BkvSFF',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_with_predefinedtype.ifc](c.ifc_filename)

Expected result: pass

## Entity matching

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[fail_entity_matching.ids](c.ids_filename)

~~~lua
#21=IfcSlab('2FOVFXFs92IecOPn1LPC_8',$,$,$,$,$,$,$,$)
~~~

[fail_entity_matching.ifc](c.ifc_filename)

Expected result: fail

## Entity subtype

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[fail_entity_subtype.ids](c.ids_filename)

~~~lua
#21=IfcWallStandardCase('2RyYh1Bun8lRg5Vz350H4d',$,$,$,$,$,$,$,$)
~~~

[fail_entity_subtype.ifc](c.ifc_filename)

Expected result: fail

## Entity case 0

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[pass_entity_case_0.ids](c.ids_filename)

~~~lua
#21=IfcWall('0WyaKlOVL99RijTaqtc01n',$,$,$,$,$,$,$,$)
~~~

[pass_entity_case_0.ifc](c.ifc_filename)

Expected result: pass

## Entity case 1

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[pass_entity_case_1.ids](c.ids_filename)

~~~lua
#21=IfcWall('22$fDL_0b4Owc0cH2oJ7aR',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_case_1.ifc](c.ifc_filename)

Expected result: pass

## Entity case 2

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[fail_entity_case_2.ids](c.ids_filename)

~~~lua
#21=IfcSlab('1R6mzWY7P81P52_2g_VaOd',$,$,$,$,$,$,$,$)
~~~

[fail_entity_case_2.ifc](c.ifc_filename)

Expected result: fail

## Entity PredefinedType 0

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>SOLIDWALL</simpleValue>
  </predefinedType>
</entity>
~~~

[fail_entity_predefinedtype_0.ids](c.ids_filename)

~~~lua
#21=IfcWall('1dZ07xq_1EUAEVr_KLcOuM',$,$,$,$,$,$,$,$)
~~~

[fail_entity_predefinedtype_0.ifc](c.ifc_filename)

Expected result: fail

## Entity PredefinedType 1

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>SOLIDWALL</simpleValue>
  </predefinedType>
</entity>
~~~

[pass_entity_predefinedtype_1.ids](c.ids_filename)

~~~lua
#21=IfcWall('1OhocE5Rj5jR6fiL9oW__w',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_predefinedtype_1.ifc](c.ifc_filename)

Expected result: pass

## Entity PredefinedType 2

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>SOLIDWALL</simpleValue>
  </predefinedType>
</entity>
~~~

[fail_entity_predefinedtype_2.ids](c.ids_filename)

~~~lua
#21=IfcWall('0VVj09j$584fkF4dfIdR5l',$,$,$,$,$,$,$,.PARTITIONING.)
~~~

[fail_entity_predefinedtype_2.ifc](c.ifc_filename)

Expected result: fail

## Entity user-defined type

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>WALDO</simpleValue>
  </predefinedType>
</entity>
~~~

[pass_entity_user-defined_type.ids](c.ids_filename)

~~~lua
#21=IfcWall('1o6I0XbGT2NBM6$UG$UDfb',$,$,$,'WALDO',$,$,$,.USERDEFINED.)
~~~

[pass_entity_user-defined_type.ifc](c.ifc_filename)

Expected result: pass

## Entity ElementType

~~~xml
<entity>
  <name>
    <simpleValue>IfcWallType</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>WALDO</simpleValue>
  </predefinedType>
</entity>
~~~

[pass_entity_elementtype.ids](c.ids_filename)

~~~lua
#21=IfcWallType('2fFUD2xqj2VOlWiesuxMTf',$,$,$,$,$,$,$,'WALDO',.USERDEFINED.)
~~~

[pass_entity_elementtype.ifc](c.ifc_filename)

Expected result: pass

## Entity no USERDEFINED

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>USERDEFINED</simpleValue>
  </predefinedType>
</entity>
~~~

[fail_entity_no_userdefined.ids](c.ids_filename)

~~~lua
#21=IfcWall('3KTte5Ey1EkOEcTt50lXWq',$,$,$,'WALDO',$,$,$,.USERDEFINED.)
~~~

[fail_entity_no_userdefined.ifc](c.ifc_filename)

Expected result: fail

## Entity PredefinedType inheritance 0

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>X</simpleValue>
  </predefinedType>
</entity>
~~~

[pass_entity_predefinedtype_inheritance_0.ids](c.ids_filename)

~~~lua
#21=IfcWall('1pLQFhGt5EHAvPOpaJrSjp',$,$,$,$,$,$,$,$)
#23=IfcRelDefinesByType('1$0jFeL95A7hX5WUTdxXDU',$,$,$,(#21),#22)
#22=IfcWallType('1cmkBO7BT0$RMWEpfm3m2r',$,$,$,$,$,$,$,'X',.USERDEFINED.)
~~~

[pass_entity_predefinedtype_inheritance_0.ifc](c.ifc_filename)

Expected result: pass

## Entity PredefinedType inheritance 1

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
  <predefinedType>
    <simpleValue>X</simpleValue>
  </predefinedType>
</entity>
~~~

[pass_entity_predefinedtype_inheritance_1.ids](c.ids_filename)

~~~lua
#21=IfcWall('1sTeQ2W4r7dwGLqO0xS1y2',$,$,$,'X',$,$,$,.USERDEFINED.)
#23=IfcRelDefinesByType('0wBw4L0zTBggCorO5Ll692',$,$,$,(#21),#22)
#22=IfcWallType('14r_IfOC51KfSOdd7_wYwn',$,$,$,$,$,$,$,$,.NOTDEFINED.)
~~~

[pass_entity_predefinedtype_inheritance_1.ifc](c.ifc_filename)

Expected result: pass

## Entity enumeration 0

~~~xml
<entity>
  <name>
    <xs:restriction base="xs:string">
      <xs:enumeration value="IfcWall"/>
      <xs:enumeration value="IfcSlab"/>
    </xs:restriction>
  </name>
</entity>
~~~

[pass_entity_enumeration_0.ids](c.ids_filename)

~~~lua
#21=IfcWall('3VSAN7SLXAV8iep0MkUu5y',$,$,$,$,$,$,$,$)
~~~

[pass_entity_enumeration_0.ifc](c.ifc_filename)

Expected result: pass

## Entity enumeration 1

~~~xml
<entity>
  <name>
    <xs:restriction base="xs:string">
      <xs:enumeration value="IfcWall"/>
      <xs:enumeration value="IfcSlab"/>
    </xs:restriction>
  </name>
</entity>
~~~

[pass_entity_enumeration_1.ids](c.ids_filename)

~~~lua
#21=IfcSlab('07pRkpVX14xupCxP4M2UAu',$,$,$,$,$,$,$,$)
~~~

[pass_entity_enumeration_1.ifc](c.ifc_filename)

Expected result: pass

## Entity enumeration 2

~~~xml
<entity>
  <name>
    <xs:restriction base="xs:string">
      <xs:enumeration value="IfcWall"/>
      <xs:enumeration value="IfcSlab"/>
    </xs:restriction>
  </name>
</entity>
~~~

[fail_entity_enumeration_2.ids](c.ids_filename)

~~~lua
#21=IfcBeam('3MZB8oUMf0aB5_Yt_qgaxI',$,$,$,$,$,$,$,$)
~~~

[fail_entity_enumeration_2.ifc](c.ifc_filename)

Expected result: fail

## Entity pattern 0

~~~xml
<entity>
  <name>
    <xs:restriction base="xs:string">
      <xs:pattern value="Ifc.*Type"/>
    </xs:restriction>
  </name>
</entity>
~~~

[fail_entity_pattern_0.ids](c.ids_filename)

~~~lua
#21=IfcWall('1JFC97UZv4AeY4Gf9w$OAg',$,$,$,$,$,$,$,$)
~~~

[fail_entity_pattern_0.ifc](c.ifc_filename)

Expected result: fail

## Entity pattern 1

~~~xml
<entity>
  <name>
    <xs:restriction base="xs:string">
      <xs:pattern value="Ifc.*Type"/>
    </xs:restriction>
  </name>
</entity>
~~~

[pass_entity_pattern_1.ids](c.ids_filename)

~~~lua
#21=IfcWallType('2CsgrfQOL7wObJibTUcLXm',$,$,$,$,$,$,$,$,.ELEMENTEDWALL.)
~~~

[pass_entity_pattern_1.ifc](c.ifc_filename)

Expected result: pass

