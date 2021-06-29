# OPEX ASpace 01

Minimal OPEX package with ArchivesSpace sync information  

```bash
├── container_ASpace_01
│   └── archival_object_3297557
│       ├── archival_object_3297557.opex
│       └── collection_ASpace_01
│           ├── asset
│           ├── asset.opex
│           └── collection_ASpace_01.opex

```



container can be zipped and ingested with ingest (v6)  

****

For ArchivesSpace sync, metadata needs to be included in `.opex` files at multiple levels:



**[archival_object_3297557.opex](archival_object_3297557.opex)**

```xml
<opex:Properties>
    <opex:Identifiers>
        <!-- Archival object ref here -->
      <opex:Identifier type="code">archival_object_3297557</opex:Identifier>
    </opex:Identifiers>
  </opex:Properties>
  <opex:DescriptiveMetadata>
    <LegacyXIP xmlns="http://preservica.com/LegacyXIP">
        <Virtual>false</Virtual>
    </LegacyXIP>
  </opex:DescriptiveMetadata>
```



**[collection_ASpace_01.opex](collection_ASpace_01.opex)**

```xml
  <DescriptiveMetadata>
    <!-- needed for sync -->
    <LegacyXIP xmlns="http://preservica.com/LegacyXIP">
      <AccessionRef>catalogue</AccessionRef>
    </LegacyXIP>
  </DescriptiveMetadata>
```




#### Contact:
David Cirella  
[github.com/decirella](https://github.com/decirella)