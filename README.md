# PDF-Splitter

1. Scans every page for city/state/zip patterns
2. Builds a frequency table of all addresses found
3. High-frequency addresses = sender (company return address, appears on every page)
4. Low-frequency addresses = customer (recipient, appears once or twice)
5. Customer boundaries = wherever a new low-frequency address appears
6. Extracts customer name from the lines above the address
7. Splits the PDF at those boundaries into individual customer files
8. Uploads each to Supabase under the client's Aftersamples collection
