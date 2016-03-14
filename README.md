#  OpenLAP-Visualizer-Starter

## Introduction

This repository contains the Maven archetype project. This project can be used to generate a starter project to quick start
development of a new `VisualizationMethod` along with its `DataTransformer` belonging to a `VisualizationFramework`.
Before getting into the guide on how to generate a skeleton starter project let's list down the terminologies that will
be used in this document:

<ul>
    <li><strong>VisualizationFramework</strong> : A web visualization library/framework which can be utilized to create interactive visualizations. For example, d3.js, dygraphs etc.</li>
    <li><strong>VisualizationMethod</strong> : A concrete interactive visualization, for example, bar chart, pie chart etc.</li>
    <li><strong>DataTransformer</strong> : A concrete implementation which transforms data received from the client in the form of the OLAPDataSet into a structure understandable by
      the VisualizationMethod that uses it</li>
</ul>

## Usage Guide

### Prerequisites

<ul>
    <li> A working version of maven </li>
    <li> Git client </li>
</ul>

### Creating a starter project

In order to generate a starter project first clone this repository on your local system and then build the Archetype project with maven using the command `mvn install`.
After building the project use the following command to generate the starter project :
</br>
```
mvn archetype:generate 
    -DarchetypeGroupId=de.rwthaachen.openlap -DarchetypeArtifactId=rwth-openlap-visualizer-framework-archetype -DarchetypeVersion=1.0 
    -DgroupId=de.rwthaachen.openlap -DartifactId=openlap-visualizer-framework-sample-combined -Dversion=1.0
```
</br>
The maven archetype command to generate the starter project takes parameters such as the `archetypeVersion` which should be adapted based on the archetype version you checked out. In addition, the command takes the `groupId`, `artifactId` and the `version` to be
inserted as arguments in the pom.xml file of the generated project. </br>
Once the generation is complete the project can imported as a Maven project into the IDE of your choosing. The generated project contains a sample implementation of the `VisualizationCodeGenerator`,the class which contains a concrete implementation of a `VisualizationMethod`. This sample class simply overrides the methods and does not provide an actual visualization code. Another sample class generated is that which implements the `DataTransformer` interface. The purpose of these sample classes is to show the developer which classes they need to provide concrete implementations for, in order to add a new visualization to the OpenLAP-Visualizer.

### Further Information
* "Maven Archetype ,  https://maven.apache.org/archetype/index.html"

