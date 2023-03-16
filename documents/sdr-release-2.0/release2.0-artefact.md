# Study Definition Repository (SDR) - Release Version 2.0

The below is the list of artefacts summarizing the list of changes in SDR to support Unified Study Definition Model (USDM) V1.9. It also explains the SDR Features at a high level.

### Sample Study JSON
- [USDM V1.0 Study JSON](ddf-sdr-sample-json(usdm-v1.0).json)

- [USDM V1.9 Study JSON](ddf-sdr-sample-json(usdm-v1.9).json) (_Latest_)

### Summary of USDM Changes (Changelog from USDM V1.0 to V1.9)
Refer to this [worksheet](usdm-v1.9-model-changes-conformance-rules.xlsx) to get list of changes on the USDM including updates to Conformance Rule.

### SDR Feature Updates
#### SDR Data Model Changes
The SDR Data Model now conforms to USDM version V1.0 and V1.9. V1.9 includes Biomedical Concepts, SoA Timepoints and other minor USDM changes detailed in the section above.

#### SDR API
- UUID Management - SDR will generate and maintain a unique identifier for a study at the parent element level. All other study element identifiers can be passed and maintained by study builders creating & updating studies in SDR. Reference Integrity checks will be performed by SDR for user managed identifiers.
- USDM Versioning – Study definitions based on USDM (Version 1.0 & 1.9) released by CDISC as part of Digital Data Flow - Phase 1 & 2 are now supported in SDR.
- Version specific API Endpoints -  Study USDM version specific endpoints will allow users to create studies conforming to a specific version (1 major and any related minor versions) of USDM and validate the study against conformance rules corresponding to that version.
- Change Audit Log - Each change submitted to SDR is tracked by the Change Audit feature built into SDR. The Http trigger will capture details of elements changed in the POST and PUT requests into a separate collection.
- Common Protocol Template (CPT) Export API - A new endpoint has been created to export study details mapped to limited set of CPT Variables grouped by sections of Common Protocol Template. Mapping Sheet from SDR fields to CPT variables is available [here](usdm-cpt-mapping-sheet.xlsx)

#### SDR UI
- Certificate-based authentication removed - Users can now access SDR UI without the need to install a valid client certificate.
- SoA Matrix - For studies conforming to V1.9 and above, the SoA Matrix View is available from the Study Details page to view Schedule of activities for each timeline under each study design within a given study.
- **For Admin Users**
  - System Usage Report & Export - The System Usage Report has been enhanced to allow users to search API usage statistics for a given date range (upto a maximum of 30 days range). Users can now also export the report into CSV format (upto a maximum of 1500 rows).
- Other changes include,
  - USDM version column on Search in UI
  - Minor UX updates

### SDR API Endpoints
[SDR API Endpoints](ddf-sdr-api-list-of-routes.xlsx) worksheet lists the active API Endpoints on the SDR added/modified as a part of SDR Release V2.0.
> **Note**:The usdmVersion is now a mandatory header parameter for all version-specific endpoints in addition to the authentication token in the HTTP request.

### Important Links to Digital Data Flow Program
- [TransCelerate Digital Data Flow](https://www.transceleratebiopharmainc.com/initiatives/digital-data-flow/)
- [CDISC DDF](https://www.cdisc.org/ddf)
- [CDISC DDF Reference Architecture Repository](https://github.com/cdisc-org/DDF-RA)
