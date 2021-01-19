# snow-data-validation
Template for bespoke data validation using stored procedures and ANSI SQL on Snowflake

## Overview
Snowflake customers use a variety of tools as part of a larger solution to build enterprise grade, integrated systems that are automated and provide value to the business. Snowflake partners like Informatica, Matillion, dbt, Talend and Qlik provide data quality and data validation components as part of their tools. In many cases these companies have built in quality rules that check for data types, null values, proper encoding and other generic data rules that can be applied for multiple customers without prior knowledge of the data points. These powerful tools can be further customized for business specific data rules for bespoke validation of all data providing 100% validation coverage for data loaded into Snowflake. These tools are becoming cheaper and more powerful as time passes, but that doesn't always mean they are easy to deploy, manager, or easy to procure. Some organizations still have a litany of compliance factors that stand in the way even after other details have been worked out. Therefore, it's not always feasible to tools from the partner ecosystem especially if Snowflake can be leveraged to solve this problem.

To help Snowflake customers think about best practices for how they might implement a solution sans tools, we have developed a couple of examples that might help with developing or modifying these options for your own data warehouse. The Snowflake Professional Services team and Systems Integrators can assist with or implement processes like these. And it is worth noting that code provided as a template or as an example 
<hr>

## Methods

### Method 1 - Dynamic Common Table Expression (CTE) from Business Rules 
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
