# haml
HLA Antibody Markup Language - For antibody assay results and expert interpretation

## Version 0.1:

Started with HAMLCase_ver1_LG.xml (renamed to sample_file_haml_0_1.xml)

Generated XSD from XML using https://www.freeformatter.com/xsd-generator.html#ad-output

I like this XML generator because it doesn’t indent the XSD nearly as much.

This XSD has no restrictions.

xmllint --schema haml__version_0_1.xsd sample_file_haml_0_1.xml

sample_file_haml_0_1.xml validates

## Version 0.2:

XML Validation Error that was very difficult to fix:

xmllint --schema haml__version_0_2.xsd sample_file_haml_0_2.xml

haml__version_0_2.xsd:22: element sequence: Schemas parser error : Element '{http://www.w3.org/2001/XMLSchema}complexType': The content is not valid. Expected is (annotation?, (simpleContent | complexContent | ((group | all | choice | sequence)?, ((attribute | attributeGroup)*, anyAttribute?)))).

## Version 0.3:

Created by backfilling the restrictions of 0.2 into the previous haml.xsd.

xmllint --schema haml__version_0_3.xsd sample_file_haml_0_3.xml

sample_file_haml_0_3.xml validates