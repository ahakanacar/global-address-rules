Global Address and Postal Code Standards Dataset
A high-quality, production-ready dataset containing address formatting standards, postal code validation regular expressions (regex), and localized address keywords (streets, neighborhoods, units) for all 249 countries and territories in the world.

This repository hosts clean, validated geocoding metadata and address parsing rules ready to be integrated into checkout forms, logistics pipelines, CRM databases, or global shipping software.

Dataset Scope & Coverage
Countries Covered: 249 sovereign countries and autonomous regions (indexed by ISO 3166-1 Alpha-3 codes).
Data Fields: Official country names, postal code regular expressions, address format masks, and translation lists for street, neighborhood, and unit keywords.
Output Formats & Files
This dataset is available in three formats to suit different engineering and analysis workflows:

1. global-address-rules.json
A structured JSON configuration file mapping rules by country ISO-3166 Alpha-3 code. Ideal for client-side JavaScript validations, node libraries, or config integrations.

Example schema: { "TUR": { "country_name": "Turkey", "postal_code_regex": "^\d{5}
⚠️ Failed to render LaTeX: KaTeX parse error: Expected 'EOF', got '}' at position 234: …"]
}
}̲,
"USA": {
…
",
      "address_format_mask": "%M %S No: %N D: %I\\n%P %C",
      "keywords": {
        "street": ["caddesi", "cad", "sokağı", "sok"],
        "neighborhood": ["mahallesi", "mah"],
        "unit": ["daire", "apartman"]
      }
    },
    "USA": {
      "country_name": "United States",
      "postal_code_regex": "^\\d{5}(-\\d{4})?", "address_format_mask": "%N %S %I\n%C, %P %Z", "keywords": { "street": ["street", "st", "road", "rd", "avenue", "ave"], "neighborhood": ["neighborhood", "suburb"], "unit": ["apartment", "apt", "unit", "suite"] } } }

2. global-address-rules.csv
A flat table formatted with a UTF-8 BOM prefix, designed for SQL database imports (COPY / IMPORT commands) into PostgreSQL, MySQL, BigQuery, or Snowflake without character corruption.

Multiple values within list columns (like keywords) are joined using the pipe character | (e.g., street|st|road).
Headers: iso_alpha3, country_name, postal_code_regex, address_format_mask, street_keywords, neighborhood_keywords, unit_keywords
3. global-address-rules.xlsx
An Excel spreadsheet designed for business analysis and pivots.

Frozen header row styled with a dark navy background.
Auto-fitted column widths for readability.
Wrap-text enabled for multi-line format masks.
Schema Attributes Reference
%S: Street / Road Name
%N: Building / House Number
%I: Unit / Suite / Apartment Number
%C: City / Town / Locality
%P: State / Province / Region
%M: Neighborhood / Suburb
%Z: Postcode / Zip Code
License
This dataset is open-source and available under the MIT License. Feel free to use, modify, and distribute it in your applications.

