## Non-existent entity name

~~~xml
<entity>
  <name>
    <simpleValue>IfcRabbit</simpleValue>
  </name>
</entity>
~~~

[fail_non-existent_entity_name.ids](fail_non-existent_entity_name.ids)

~~~lua
#21=IfcWall('2uQQovhan3bB1poxQLMhfn',$,$,$,$,$,$,$,$)
~~~

[fail_non-existent_entity_name.ifc](fail_non-existent_entity_name.ifc)

Expected result: fail

## Entity matching

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[pass_entity_matching.ids](pass_entity_matching.ids)

~~~lua
#21=IfcWall('0Gbh0t8qz6VRGiSKRrrwLf',$,$,$,$,$,$,$,$)
~~~

[pass_entity_matching.ifc](pass_entity_matching.ifc)

Expected result: pass

## Entity with PredefinedType

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[pass_entity_with_predefinedtype.ids](pass_entity_with_predefinedtype.ids)

~~~lua
#21=IfcWall('0EX4$8SBPA7A0Lnqx1Xrvw',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_with_predefinedtype.ifc](pass_entity_with_predefinedtype.ifc)

Expected result: pass

## Entity matching

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[fail_entity_matching.ids](fail_entity_matching.ids)

~~~lua
#21=IfcSlab('0eHitfrVfFqeqNrEGhNtLI',$,$,$,$,$,$,$,$)
~~~

[fail_entity_matching.ifc](fail_entity_matching.ifc)

Expected result: fail

## Entity subtype

~~~xml
<entity>
  <name>
    <simpleValue>IfcWall</simpleValue>
  </name>
</entity>
~~~

[fail_entity_subtype.ids](fail_entity_subtype.ids)

~~~lua
#21=IfcWallStandardCase('3FPmTzEo917fmYJ4Pni2iq',$,$,$,$,$,$,$,$)
~~~

[fail_entity_subtype.ifc](fail_entity_subtype.ifc)

Expected result: fail

## Entity case 0

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[pass_entity_case_0.ids](pass_entity_case_0.ids)

~~~lua
#21=IfcWall('3qH0QMfe5DhRuQr830Eb$5',$,$,$,$,$,$,$,$)
~~~

[pass_entity_case_0.ifc](pass_entity_case_0.ifc)

Expected result: pass

## Entity case 1

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[pass_entity_case_1.ids](pass_entity_case_1.ids)

~~~lua
#21=IfcWall('0BTDYfB413wf675etQgd1$',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_case_1.ifc](pass_entity_case_1.ifc)

Expected result: pass

## Entity case 2

~~~xml
<entity>
  <name>
    <simpleValue>IFCWALL</simpleValue>
  </name>
</entity>
~~~

[fail_entity_case_2.ids](fail_entity_case_2.ids)

~~~lua
#21=IfcSlab('3MIRhGw2z2R8nMvEBvuAbh',$,$,$,$,$,$,$,$)
~~~

[fail_entity_case_2.ifc](fail_entity_case_2.ifc)

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

[fail_entity_predefinedtype_0.ids](fail_entity_predefinedtype_0.ids)

~~~lua
#21=IfcWall('1oG9TNQu50h81t7dIqemfQ',$,$,$,$,$,$,$,$)
~~~

[fail_entity_predefinedtype_0.ifc](fail_entity_predefinedtype_0.ifc)

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

[pass_entity_predefinedtype_1.ids](pass_entity_predefinedtype_1.ids)

~~~lua
#21=IfcWall('2CMYVfzbPAtxHOZqMBnEeS',$,$,$,$,$,$,$,.SOLIDWALL.)
~~~

[pass_entity_predefinedtype_1.ifc](pass_entity_predefinedtype_1.ifc)

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

[fail_entity_predefinedtype_2.ids](fail_entity_predefinedtype_2.ids)

~~~lua
#21=IfcWall('1sauVNV5v9NAex0k854XL6',$,$,$,$,$,$,$,.PARTITIONING.)
~~~

[fail_entity_predefinedtype_2.ifc](fail_entity_predefinedtype_2.ifc)

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

[pass_entity_user-defined_type.ids](pass_entity_user-defined_type.ids)

~~~lua
#21=IfcWall('0$XmJWyev9R8vlmHJwH6$n',$,$,$,'WALDO',$,$,$,.USERDEFINED.)
~~~

[pass_entity_user-defined_type.ifc](pass_entity_user-defined_type.ifc)

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

[pass_entity_elementtype.ids](pass_entity_elementtype.ids)

~~~lua
#21=IfcWallType('1LxNRQHaX4OxICCxs2tqe2',$,$,$,$,$,$,$,'WALDO',.USERDEFINED.)
~~~

[pass_entity_elementtype.ifc](pass_entity_elementtype.ifc)

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

[fail_entity_no_userdefined.ids](fail_entity_no_userdefined.ids)

~~~lua
#21=IfcWall('23Si_bNInCi8qWOXmdGSC1',$,$,$,'WALDO',$,$,$,.USERDEFINED.)
~~~

[fail_entity_no_userdefined.ifc](fail_entity_no_userdefined.ifc)

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

[pass_entity_predefinedtype_inheritance_0.ids](pass_entity_predefinedtype_inheritance_0.ids)

~~~lua
#21=IfcWall('0tPssAvvvBH8DFNru0lho2',$,$,$,$,$,$,$,$)
#23=IfcRelDefinesByType('0hDtVGWHD7OR76ybfgY3iT',$,$,$,(#21),#22)
#22=IfcWallType('0XcYqjFNvDAuSJhqGKBBeV',$,$,$,$,$,$,$,'X',.USERDEFINED.)
~~~

[pass_entity_predefinedtype_inheritance_0.ifc](pass_entity_predefinedtype_inheritance_0.ifc)

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

[pass_entity_predefinedtype_inheritance_1.ids](pass_entity_predefinedtype_inheritance_1.ids)

~~~lua
#21=IfcWall('1WeLhPLHL3DxOO4A2vFbiG',$,$,$,'X',$,$,$,.USERDEFINED.)
#23=IfcRelDefinesByType('0EJtgFA8n1BhnnuLUoN2u7',$,$,$,(#21),#22)
#22=IfcWallType('2EF3ruS05DARkfL87dA$T$',$,$,$,$,$,$,$,$,.NOTDEFINED.)
~~~

[pass_entity_predefinedtype_inheritance_1.ifc](pass_entity_predefinedtype_inheritance_1.ifc)

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

[pass_entity_enumeration_0.ids](pass_entity_enumeration_0.ids)

~~~lua
#21=IfcWall('2g2Kx_b6v6qONlgiS2rQ3n',$,$,$,$,$,$,$,$)
~~~

[pass_entity_enumeration_0.ifc](pass_entity_enumeration_0.ifc)

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

[pass_entity_enumeration_1.ids](pass_entity_enumeration_1.ids)

~~~lua
#21=IfcSlab('0eZem_Cb538hBFyKciQs4v',$,$,$,$,$,$,$,$)
~~~

[pass_entity_enumeration_1.ifc](pass_entity_enumeration_1.ifc)

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

[fail_entity_enumeration_2.ids](fail_entity_enumeration_2.ids)

~~~lua
#21=IfcBeam('2Rry_D_gn2YvK3cw9A$lts',$,$,$,$,$,$,$,$)
~~~

[fail_entity_enumeration_2.ifc](fail_entity_enumeration_2.ifc)

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

[fail_entity_pattern_0.ids](fail_entity_pattern_0.ids)

~~~lua
#21=IfcWall('0RvYRGIQ98_ftIKp46Y2uA',$,$,$,$,$,$,$,$)
~~~

[fail_entity_pattern_0.ifc](fail_entity_pattern_0.ifc)

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

[pass_entity_pattern_1.ids](pass_entity_pattern_1.ids)

~~~lua
#21=IfcWallType('3aX2NlvpT5zOXwUkDY0r_o',$,$,$,$,$,$,$,$,.ELEMENTEDWALL.)
~~~

[pass_entity_pattern_1.ifc](pass_entity_pattern_1.ifc)

Expected result: pass

