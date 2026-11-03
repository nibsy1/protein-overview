# Curated data-access layer (APIs + cache + rate limits)

## Summary
Build the fixed, versioned toolset of REST APIs plus web-search fallback, with response caching and polite rate limiting.

## Details
- APIs: UniProt, NCBI eUtils, InterPro, AlphaFold DB, Expression Atlas; clade databases (TAIR, MGI, ZFIN, RGD, FlyBase, WormBase, SGD, Ensembl Plants/Fungi/Protists, Bgee); orthology (OrthoDB, OMA, PANTHER, eggNOG); interactions (STRING, BioGRID); TCDB.
- Every fetched fact cached into the store with query URL and timestamp (reproducibility + audit).
- Unreachable/empty source: retry, then alternative source, only then record "absence of data" as a finding.

## Acceptance criteria
- Toolset versioned; cache writes URL+timestamp; rate-limit handling tested against at least UniProt and NCBI.

Ref: PRD §5
