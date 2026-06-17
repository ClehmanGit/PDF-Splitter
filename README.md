# PDF-Splitter

Scans every page for city/state/zip patterns
Builds a frequency table of all addresses found
High-frequency addresses = sender (company return address, appears on every page)
Low-frequency addresses = customer (recipient, appears once or twice)
Customer boundaries = wherever a new low-frequency address appears
Extracts customer name from the lines above the address
Splits the PDF at those boundaries into individual customer files
Uploads each to Supabase under the client's Aftersamples collection
