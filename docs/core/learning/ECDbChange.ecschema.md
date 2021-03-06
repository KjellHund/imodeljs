---
Schema: ECDbChange
This file was automatically generated via ecjson2md. Do not edit this file. Any edits made to this file will be overwritten the next time it is generated
---

# ECDbChange ECSchema

## Classes

### ChangeSummary

**Class Type:** EntityClass

**Class Properties:**

|    Name    |    Description    |    Type    |      Extended Type     |
|:-----------|:------------------|:-----------|:-----------------------|
|ExtendedProperties||string|Json|
|            |                   |            |                        |

### ChangeSummaryContainsInstanceChanges

**Class Type:** RelationshipClass

**Relationship Class:**

|          |    ConstraintClasses    |            Multiplicity            |
|:---------|:------------------------|:-----------------------------------|
|**Source**|ChangeSummary|(1..1)|
|**Target**|InstanceChange|(0..*)|
|          |                         |                                    |

### InstanceChange

Represents an instance change in a change summary

**Class Type:** EntityClass

**Class Properties:**

|    Name    |    Description    |    Type    |      Extended Type     |
|:-----------|:------------------|:-----------|:-----------------------|
|Summary||||
|ChangedInstance|Key of the change instance|||
|OpCode||OpCode||
|IsIndirect|Change happened due to a foreign key action or trigger|boolean||
|            |                   |            |                        |

### InstanceChangeOwnsPropertyValueChanges

**Class Type:** RelationshipClass

**Relationship Class:**

|          |    ConstraintClasses    |            Multiplicity            |
|:---------|:------------------------|:-----------------------------------|
|**Source**|InstanceChange|(1..1)|
|**Target**|PropertyValueChange|(0..*)|
|          |                         |                                    |

### InstanceKey

**Class Type:** StructClass

**Class Properties:**

|    Name    |    Description    |    Type    |      Extended Type     |
|:-----------|:------------------|:-----------|:-----------------------|
|Id||long|Id|
|ClassId||long|Id|
|            |                   |            |                        |

### PropertyValueChange

Represents an property value change of an instance change in a change summary

**Class Type:** EntityClass

**Class Properties:**

|    Name    |    Description    |    Type    |      Extended Type     |
|:-----------|:------------------|:-----------|:-----------------------|
|InstanceChange||||
|AccessString||string||
|RawOldValue|Untyped old value|binary||
|RawNewValue|Untyped new value|binary||
|            |                   |            |                        |

