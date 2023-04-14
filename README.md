# opcUa-aasV3-nodeset2
Asset Administration Shell V3.0RC02 meta-model on OPC UA
In development

## Description

This implementation is inspired by the deprecated [OPC 30270](https://opcfoundation.org/developer-tools/documents/view/273) Industry 4.0 Asset Administration Shell specification.

## Implementation

### Primitive Types
The primitive type defined in the specification Details of the Asset Administration Shell part 1 [V3.0RC02](https://www.plattform-i40.de/IP/Redaktion/EN/Downloads/Publikation/Details_of_the_Asset_Administration_Shell_Part1_V3.html) Chapter 5.7.12.2 are derived from the OPC UA type as follow:
 |AAS | OPC UA|
 |---|---|
 | BlobType | ByteString |
 |Identifier, ContentType, <br>PathType, QualifierType | String |
 |LangStringSet | LocalizedText |

ValueDataType is simply replaced by the OPC UA BaseDataType.

### Enumerations
Every Enumeration declares all members, even if they are a set of other enumerations, as enumerations cannot derive from each other.

### Classes
All abstract classes are derived from OPC UA BaseInterfaceType. The non-abstract classes are derived from BaseObjectType.

### Other notes

 - Attributes of type "ModelReference<{Referable}>" are declare using a placeholder type. (Attributes fund in classes: Extension, EventPayload, BasicEventElement, and AssetAdministrationShell)
 - Attributes of type dateTime use directly the OPC UA dateTime type.
 - Attribute timestamp in class EventPayload is declared using OPC UA dateTime type instead of the unknown dateTimeStamp type.
 - Attribute typeValueListElement in class SubmodelElementList is declared using AAS SubmodelElement type instead of the unknown SubmodelElementElements type.
 - Inheritance could be wrongly implemented
