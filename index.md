---
title: Markdown test page
layout: flat
---

The following table goes through the schema line-by-line and details the modifications required to create a new OVAL Test.  For simplicity, the OVAL Test’s name “file” is replaced with “[\*]”.
<table>
  <tr>
    <th>Line(s)</th>
    <th>What changes?</th>
  </tr>
  <tbody>
    <tr>
      <td>01</td>
      <td>The <span style="font-family: 'Courier New'">name</span> attribute is assigned a value of “[\*]_test” in accordance with [Section 4.2.2](#4-2-2-tests).</td>
    </tr>
    <tr>
      <td>03</td>
      <td>The <span style="font-family: 'Courier New'">documentation</span> element describes what endpoint metadata this particular OVAL Test is designed to collect and evaluate.  Any necessary clarifications to the scope of this OVAL Test should be provided here. </td>
    </tr>
	<tr>
      <td>05-09</td>
      <td>The <span style="font-family: 'Courier New'">element_mapping</span> construct explicitly correlates the associated OVAL Test, Object, State, and Item constructs and must always be present.
	<br/><br/>In most cases, the relevant OVAL Test name should be used to update the test, object, state, and item components of the <span style="font-family: 'Courier New'">element_mapping</span> construct with [\*]_test, [\*]_object, [\*]_state, and [\*]_item. With that said, it is important to note that it is also possible to map new OVAL Tests to existing OVAL Items as exemplified with the <span style="font-family: 'Courier New'">win-def:fileeffectiverights53_test</span> and <span style="font-family: 'Courier New'">win-sc:fileeffectiverights_item</span>.
	<br/><br/>The <span style="font-family: 'Courier New'">target_namespace</span> attribute identifies the namespace URI of the platform-specific OVAL System Characteristics Model associated with the OVAL Test.</td>
    </tr>
	<tr>
      <td>23-32</td>
      <td>This <span style="font-family: 'Courier New'">complexType</span> element must always be present and verbatim for every OVAL Test. Every OVAL Test extends the <span style="font-family: 'Courier New'">oval-def:TestType</span> construct and contains one <span style="font-family: 'Courier New'">object</span> element followed by zero or more <span style="font-family: 'Courier New'">state</span> elements.</td>
    </tr>
  </tbody>
</table>
