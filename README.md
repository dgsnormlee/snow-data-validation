# snow-data-validation
Template for bespoke data validation using stored procedures and ANSI SQL on Snowflake

## Overview
Snowflake customers use a variety of tools as part of a larger solution to build enterprise grade, integrated systems that are automated and provide value to the business. Snowflake partners like Informatica, Matillion, dbt, Talend and Qlik provide data quality and data validation components as part of their tools. In many cases these companies have built in quality rules that check for data types, null values, proper encoding and other generic data rules that can be applied for multiple customers without prior knowledge of the data points. These powerful tools can be further customized for business specific data rules for bespoke validation of all data providing 100% validation coverage for data loaded into Snowflake. These tools are becoming cheaper and more powerful as time passes, but that doesn't always mean they are easy to deploy, manager, or easy to procure. Some organizations still have a litany of compliance factors that stand in the way even after other details have been worked out. Therefore, it's not always feasible to tools from the partner ecosystem especially if Snowflake can be leveraged to solve this problem.

To help Snowflake customers think about best practices for how they might implement a solution sans tools, we have developed a couple of examples that might help with developing or modifying these options for your own data warehouse. The Snowflake Professional Services team and Systems Integrators can assist with or implement processes like these. But it is worth noting that code provided as a template or as an example can assist customers in thinking through the process of implementing this pipeline or developing a strategy to support this. In traditional architectures, the limitations of compute and storage has forced focus of resources on the management of these resources; with Snowflake these responsibilities disappear and allow business to focus on devliering results with the data.
<hr>

## Methods
The following methods used to validate data have their own unique advantages and disadvantages. Consider these as examples for building your own pipelines are relevant to your own data assets.
<img src="images/Data_Validation_w_ Notes.png" alt="Data Validation" title="Data Validation" />
In both of the following methods, data comes from an external source. There are three distinct routes to load data into Snowflake. One route is to be  Extracted and Loaded through an ETL/ELT tool or custom application (e.g. python) and delivered to a staging table in Snowflake. Alternatively, data is loaded into a customer managed blob store (i.e. AWS S3, Azure Blob/ADLSG2, or GCP GCS) where Snowflake can be granted direct access to the relative location through an [External Stage](https://docs.snowflake.com/en/user-guide/data-load-bulk.html). Similarly, SnowSQL or the WebUI (with a compressed 50MB limitation for hte UI) can be used to bulk load data from an on-prem data source to a stage table. In any of those cases the primary objective is to load data into a "staging" or "landing" table in Snowflake. This table will collect all the data that is loaded into Snowflake.

The [VALIDATE](https://docs.snowflake.com/en/sql-reference/functions/validate.html) function can validate record level failures of past COPY commands. By default the COPY command will pass/fail a file that is loaded, but if the desire is to know which records have failed initial data loads then VALIDATE will be a good first stop towards 

An [External Table](https://docs.snowflake.com/en/user-guide/tables-external-intro.html) can be leveraged to preemptively access the data in a customer managed blob store where views and queries can validate the data before an attempted data load. 

Once this strategy is defined for the business for a data load process then additional business specific data rules can then be applied. Again this would be a great place for additional tooling to come into play, but if our goal is to simplify the architecture footprint or there are constraints with procuring additional tools then consider the following methods as examples for moving forward.

### Method 1 - Dynamic Common Table Expression (CTE) from Business Rules 
Method 1 describes a 
**Pros**
**Cons**

### Method 2 - Declarative Pipeline through concrete Views
**Pros**
**Cons**

## Example Data and Rules

## Maintainers

**Gabriel Mullen**
is a Senior Sales Engineer with Snowflake for the State, Local, and Education Team

**Brock Cooper**
is a Senior Sales Engineer with Snowflake for the State, Local, and Education Team

This is a community-developed script, not an official Snowflake offering. It comes with no support or warranty. However, feel free to raise a github issue if you find a bug or would like a new feature.

## Legal
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this tool except in compliance with the License. You may obtain a copy of the License at: http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
