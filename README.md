# ATT&CK Control Mappings
This repository includes tools and data for mapping control frameworks to MITRE ATT&amp;CK. In addition to mapping the frameworks, it defines a common representation for frameworks — see [control format](#control-format), below.

Control frameworks are represented via STIX2.0 bundles. Controls within control frameworks are represented as [course-of-actions](https://docs.oasis-open.org/cti/stix/v2.0/csprd01/part2-stix-objects/stix-v2.0-csprd01-part2-stix-objects.html#_Toc476230929) and their mappings ATT&CK techniques as [relationships](https://docs.oasis-open.org/cti/stix/v2.0/csprd01/part2-stix-objects/stix-v2.0-csprd01-part2-stix-objects.html#_Toc476230970) of type [mitigates]. Additional structure within the framework may be conveyed on the course-of-action with the custom field `x_mitre_control_family` (a `string` denoting the control family), and relationships of type `subcontrol-of` mapping sub-controls to their parent controls when frameworks nest controls hierarchically.