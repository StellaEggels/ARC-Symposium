# SQL_to_ARC

In the NFDI FAIRagro project we cannot several RDIs with a common middleware that is
ARC/Datahub-based. The challenge is to convert the meta data offered by those RDIs to
ARC.

On idea to tackle that is to create an SQL-to-ARC converter.

## Outline of the SQL-to-ARC converter

We assume to have access to the RDI's SQL database. We create new views in that database
that correspoond to entities within the ARC context. E.g:

* ARC_investigation
* ARC_study
* ARC_assay
* ARC_person
* ARC_sample
* ARC_sample_characteristic

Then we use an ARCtrl-based software (written in python) to perform the actual conversion.
The prototype can be found here: git@github.com:fairagro/m4.2_SQLToARC.git (currently private).