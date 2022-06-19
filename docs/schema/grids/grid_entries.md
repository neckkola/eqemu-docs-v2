# grid_entries

!!! info
	This page was last generated 2022.06.18

## Relationship Diagram

[Diagram Edit](https://mermaid.live/edit#eyJjb2RlIjoiZXJEaWFncmFtXG4gICAgZ3JpZF9lbnRyaWVzIHtcbiAgICAgICAgaW50IGdyaWRpZFxuICAgICAgICAgZ3JpZF9pZFxuICAgICAgICBpbnQgem9uZWlkXG4gICAgfVxuICAgIGdyaWQge1xuICAgICAgICBpbnQgaWRcbiAgICAgICAgaW50IHpvbmVpZFxuICAgIH1cbiAgICB6b25lIHtcbiAgICAgICAgaW50IHpvbmVpZG51bWJlclxuICAgICAgICB0aW55aW50dW5zaWduZWQgdmVyc2lvblxuICAgICAgICB2YXJjaGFyIHNob3J0X25hbWVcbiAgICAgICAgdmFyY2hhciBjb250ZW50X2ZsYWdzXG4gICAgICAgIHZhcmNoYXIgY29udGVudF9mbGFnc19kaXNhYmxlZFxuICAgIH1cbiAgICBncmlkX2VudHJpZXMgfHwtLW97IGdyaWQgOiBPbmUtdG8tT25lXG4gICAgZ3JpZF9lbnRyaWVzIHx8LS1veyB6b25lIDogT25lLXRvLU9uZVxuXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOnRydWUsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjp0cnVlfQ==){target=diagram-edit}

[![](https://mermaid.ink/img/eyJjb2RlIjoiZXJEaWFncmFtXG4gICAgZ3JpZF9lbnRyaWVzIHtcbiAgICAgICAgaW50IGdyaWRpZFxuICAgICAgICAgZ3JpZF9pZFxuICAgICAgICBpbnQgem9uZWlkXG4gICAgfVxuICAgIGdyaWQge1xuICAgICAgICBpbnQgaWRcbiAgICAgICAgaW50IHpvbmVpZFxuICAgIH1cbiAgICB6b25lIHtcbiAgICAgICAgaW50IHpvbmVpZG51bWJlclxuICAgICAgICB0aW55aW50dW5zaWduZWQgdmVyc2lvblxuICAgICAgICB2YXJjaGFyIHNob3J0X25hbWVcbiAgICAgICAgdmFyY2hhciBjb250ZW50X2ZsYWdzXG4gICAgICAgIHZhcmNoYXIgY29udGVudF9mbGFnc19kaXNhYmxlZFxuICAgIH1cbiAgICBncmlkX2VudHJpZXMgfHwtLW97IGdyaWQgOiBPbmUtdG8tT25lXG4gICAgZ3JpZF9lbnRyaWVzIHx8LS1veyB6b25lIDogT25lLXRvLU9uZVxuXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOnRydWUsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjp0cnVlfQ==)](https://mermaid.ink/img/eyJjb2RlIjoiZXJEaWFncmFtXG4gICAgZ3JpZF9lbnRyaWVzIHtcbiAgICAgICAgaW50IGdyaWRpZFxuICAgICAgICAgZ3JpZF9pZFxuICAgICAgICBpbnQgem9uZWlkXG4gICAgfVxuICAgIGdyaWQge1xuICAgICAgICBpbnQgaWRcbiAgICAgICAgaW50IHpvbmVpZFxuICAgIH1cbiAgICB6b25lIHtcbiAgICAgICAgaW50IHpvbmVpZG51bWJlclxuICAgICAgICB0aW55aW50dW5zaWduZWQgdmVyc2lvblxuICAgICAgICB2YXJjaGFyIHNob3J0X25hbWVcbiAgICAgICAgdmFyY2hhciBjb250ZW50X2ZsYWdzXG4gICAgICAgIHZhcmNoYXIgY29udGVudF9mbGFnc19kaXNhYmxlZFxuICAgIH1cbiAgICBncmlkX2VudHJpZXMgfHwtLW97IGdyaWQgOiBPbmUtdG8tT25lXG4gICAgZ3JpZF9lbnRyaWVzIHx8LS1veyB6b25lIDogT25lLXRvLU9uZVxuXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9LCJ1cGRhdGVFZGl0b3IiOnRydWUsImF1dG9TeW5jIjp0cnVlLCJ1cGRhdGVEaWFncmFtIjp0cnVlfQ==){target=diagram}


## Relationships

| Relationship Type | Local Key | Relates to Table | Foreign Key |
| :--- | :--- | :--- | :--- |
| One-to-One | grid_id | [grid](../../schema/grids/grid.md) | id |
| One-to-One | zoneid | [zone](../../schema/zone/zone.md) | zoneidnumber |

## Schema

| Column | Data Type | Description |
| :--- | :--- | :--- |
| gridid | int | [Grid Identifier](grid.md) |
| zoneid | int | [Zone Identifier](../../../../server/zones/zone-list) |
| number | int | Waypoint Identifier |
| x | float | X Coordinate |
| y | float | Y Coordinate |
| z | float | Z Coordinate |
| heading | float | Heading Coordinate |
| pause | int | Pause in Seconds |
| centerpoint | tinyint | Center Point: 0 = False, 1 = True |

