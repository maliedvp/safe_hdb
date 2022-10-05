# Table of contents
1. [Purpose](#purpose)
2. [GitHub](#github)
3. [Schema](#schema)
    1. [Database Layers](#schema_layers)
    2. [The Layers' Tables](#schema_tables)
    3. [Variable Definitions](#schema_definitions)
3. [Access](#access)
3. [Test](#test)


## Purpose <a name="purpose"></a>

This repository hosts the code and documentation associated with the SAFE historical firm database for Germany. It further provides information on how to formally [access the database](#access).

## GitHub Structure <a name="github"></a>
Note that the repository relies on GitHub submodules. Submodules can either be external stand-alone projects or repositories established only for creating the SAFE database. Moreover, running the file 

><span style="background-color:#ddd">main.py</span>.

builds all layers of the database, including descriptive statistics and graphical illustrations of the layers, from scratch. The Graph below illustrates the logic of the process. Each yellow rectangular represents a submodule.

<p align="center">
	<iframe
		title = "Flow Chart"
		src="DOCS/flowchart.html"
		style="width:90%;height:40%"
	></iframe>
</p>

## Data Model / Database Design <a name="schema"></a>

### Database Layers <a name="schema_layers"></a>

embed graph here

### The Layers' Tables <a name="schema_tables"></a>

<p align="center">
	<iframe
		title = "Input Layer"
		src="https://dbdiagram.io/d/625e67ca2514c97903536190"
		style="width:90%; height:90%;"
	></iframe>
</p>

### Variable Definitions <a name="orga_definitions"></a>

## Access <a name="access"></a>

Please contact [Dennis Gram](mailto:gram@safe-frankfurt.de), the head of the SAFE data center, for access
