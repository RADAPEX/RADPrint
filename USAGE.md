# Using RADPrint-Free

To use RADPrint-Free, you must create your own template DOCx file. An example can be found in the repository -> `https://github.com/RADAPEX/RADPrint-Free/blob/main/example_template.docx`

---

## Adding the plug in to your APEX application

1. **Navigate to your page item**

In the APEX builder, select the page item (e.g. button) you would like to use RADPrint-Free with

2. **Create a dynamic action**

Add a dynamic action to the previosuly selected button, for the true action select RADPrint-Free [Plug-In]
 
## Plugin settings

Under the settings tab in the plugin dynamic action, you must configure the following settings:

1. **Template**

There are two methods of adding your template to the plugin:

    - Paste the URL of your template file directly into the template section
    - In shared components, create a static application file and paste its reference

2. **Output Filename**

Set the name of the file that will be printed

3. **Source Type**

Set to SQL Query Returning JSON

4. **Write your query**
 
Your SQL query must return JSON objects that match the placeholders in your DOCX template.

For example, if your template has {employee_name} your JSON must include "employee_name"

```sql
SELECT JSON_OBJECT(
   'employee_name' VALUE employee_name,
   'salary'        VALUE salary
) AS json_data
FROM employee
WHERE employee_id = 100
```