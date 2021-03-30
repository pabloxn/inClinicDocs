# View Structure

| **Key**       | **Type**                       | **Required** | **Defaults** | **Description**                           |
| :------------ | :----------------------------- | :----------: | :----------: | :---------------------------------------- |
| **toolbar**   | Toolbar Structure              |      No      |              | Toolbar setup                             |
| **labels**    | Label Structure                |     Yes      |              | Text to display for no records to display |
| **structure** | Structure[]                    |      No      |              | Defaults                                  |
| **table**     | Table Structure                |     Yes      |              | Table to display                          |
| **layout?**   | ‘list’, ’inline’,’form’,’card’ |      No      |     list     | Define display                            |

## Toolbar

| **Key**          | **Type**           | **Required** | **Defaults** | **Description**                    |
| :--------------- | :----------------- | :----------: | :----------: | :--------------------------------- |
| **globalFilter** | Filter Structure[] |      N       |              | Global Filter Definition           |
| **showAdd**      | Boolean            |      N       |              | Show default Add button            |
| **buttons**      | Button Structure[] |      N       |              | Array of buttons to add to toolbar |

## Button Structure

| **Key**      | **Type**             | **Required** | **Defaults** | **Description**             |
| :----------- | :------------------- | :----------: | :----------: | :-------------------------- |
| **label**    | String               |     Yes      |              | Display text on button      |
| **icon**     | String               |      No      |              | Icon to display             |
| **link**     | String               |     Yes      |              | Path for router             |
| **primary**  | Boolean              |      No      |              | Add primary theme to button |
| **position** | String:’start’,’end’ |      No      |    start     | Start or end of toolbar row |
| **area**     | String:’main’        |   ’filter’   |      No      | main                        | Defines toolbar row to add button to. |

## Structure (Array)

| **Key**             | **Type**                   | **Required** | **Defaults** | **Description**                 |
| :------------------ | :------------------------- | :----------: | :----------: | :------------------------------ |
| **label**           | String                     |      N       |              | Display text                    |
| **key**             | String                     |      Y       |              | Field to display                |
| **type**            | String                     |      N       |              | Edit type                       |
| **LookupTable**     | String                     |      N       |              | Table to look up if foreign key |
| **columnOptions**   | Column Options Structure   |      N       |              | Column display options          |
| **templateOptions** | Template Options Structure |      N       |              | Form edit options               |
| **defaultValue**    | Any                        |      N       |              | Default value for field         |

## Table Structure

| **Key**    | **Type**           | **Required** | **Default** | **Description** |
| :--------- | :----------------- | :----------: | :---------: | :-------------- |
| **path**   | String             |      Y       |             | Table path      |
| **filter** | Filter Structure[] |      N       |             | Table filter    |
| **Sort**   | Sort Structure[]   |      N       |             | Table Sort      |

## Filter Structure (array)

| **Key**        | **Type** | **Required** | **Defaults** | **Description**       |
| :------------- | :------- | :----------: | :----------: | :-------------------- |
| **field**      | String   |      Y       |              | Field to filter by    |
| **ignoreCase** | Boolean  |      N       |              | Ignore case on filter |
| **operator**   | String   |      Y       |              | Operator for filter   |
| **value**      | String   |      Y       |              | Value to filter by    |

## Sort Structure (Array)

| **Key**   | **Type** | **Required** | **Defaults** | **Description**  |
| :-------- | :------- | :----------: | :----------: | :--------------- |
| **dir**   | String   |      Y       |              | Direction        |
| **field** | String   |      Y       |              | Field to sort by |
