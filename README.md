# inference_engine

## Overview
Functions to infer ew information out of a limited set of information. For example, if someone has an aemail address as bob.smith@companyxyz.com, then it would infer that bob works for companyxyz. 

It is understood that inferences comes with a degree of reliability. Therefore each inferences will have a reliability score attached to it. 

## Function
### Input:
- json record or list of record following schema.org jsonld schema

### Output:
- List of inferred records in schema.org jsonld schema

## Inferences

Source object | Source key | Infered object | Infered information | library | Logic | Description
--------------|------------|----------------|---------------------|---------|-------|------------
schema:person | schema:email | schema:person | schema:worksfor | None | email are correlated to employment | Assumes company is employment for non-public email (yahoo, gmail, etc)
schema:person | schema:givenname | schema:person | schema:gender | namegender | Correlation between first name and gender | Uses statistical correlation between first name and gender


