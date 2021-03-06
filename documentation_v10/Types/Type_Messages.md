---
uid: typeMessagesv10
---

# Type Messages


Types are defined using the JSON Schema specification (http://json-schema.org/). For details on supported property data types and formats, see [Type Properties and Formats](xref:typePropertiesAndFormatsv10).

Types can be created, updated, or deleted. Updating a Type without updating the Type\'s version will result in a failure. Once a Type is deleted, any operations on Containers or Data using that Type will fail.

The body of a Type message consists of an array of objects. The following keywords are used to define a Type:

| Name | Value |
| --- | --- |
| `id` | Unique identifier of the Type. |
| `classification` | One of `dynamic` or `static`.  |
| `version` | Optional version of the Type. The version must be of format x.x.x.x, where x must be an integer greater than or equal to 0. If omitted version 1.0.0.0 is assumed. |
| `name` | Optional friendly name for the Type. |
| `description` | Optional description for the Type. |
| `tags` | Optional array of strings to tag the Type. |
| `metadata` | Optional key-value pairs associated with the Type. |
| `properties` | Key-value pairs defining the properties of a Type. |
| `type` | Inherited from JSON Schema. Must be set to `object`. |

The `id` cannot begin with the character sequence __. This has been reserved for predefined Types. Currently the only supported predefined Type 
is [__Link](xref:linkTypev10). 

A `static` classification represents metadata describing a device being observed and should be used to capture data that is descriptive and relatively unchanging. 
A `dynamic` classification represents observed or calculated measurements taken from a device.


### Examples of Type Messages and Property Formats

   - [Link Type](xref:linkTypev10)
   - [Type Properties and Formats](xref:typePropertiesAndFormatsv10)   
   - [Type Message Example](xref:typeExamplev10)

