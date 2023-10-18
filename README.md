# Normalization_Assignment


## Answer 1
**Un-Normalized Form (One Big Table):**

In its un-normalized form, the data can be represented as a single table where all the information is stored together. Here is an example of the data in this format, where each row represents a school with various attributes:

| time_period | time_identifier | geographic_level | country_code | country_name | old_la_code | new_la_code | la_name | school_ukprn | school_urn | school_laestab | school_name | school_type | school_phase | trust | academy | basic_entitlement_primary | basic_entitlement_ks3 | basic_entitlement_ks4 | basic_entitlement_total_funding | fsm_funding | fsm6_funding | idaci_band_f | idaci_band_e | idaci_band_d | idaci_band_c | idaci_band_b | idaci_band_a | idaci_funding | deprivation_total_funding | lac_total_funding | eal_total_funding | mobility_total_funding | prior_attainment_total_funding | lump_sum_total_funding | sparsity_total_funding | london_fringe | split_site_total_funding | national_non_domestic_rates_funding | pfi_total_funding | exceptional_factors_total_funding | minimum_per_pupil_funding | total_schools_block_allocation_(pre_mfg) | mfg_protection_or_capping_scaling | total_schools_block_allocation_(post_mfg) | notional_sen | total_number_of_pupils | allocation_per_pupil | pupil_premium | pupil_premium_pupils | universal_infant_free_school_meals_grant | pe_&_sport_premium | pe_&_sport_premium_pupils | coronavirus_recovery_premium_funding | School_led_tutoring_funding | schools_supplementary_grant | total_funding |
|-------------|------------------|-------------------|--------------|--------------|-------------|-------------|---------|--------------|------------|-----------------|-------------|--------------|--------------|-------|---------|---------------------------|------------------------|------------------------|------------------------------|-------------|--------------|--------------|--------------|--------------|--------------|--------------|--------------|--------------|---------------------------|---------------------|--------------------|-----------------------|----------------------------------|-----------------------|------------------------|------------------|--------------------------|------------------------------------|-------------------|-----------------------------------|-----------------------------|----------------------------------------|---------------------------------|----------------------------------------|---------------|-------------------------|-------------------------|----------------------|--------------------------|------------------------------------------|----------------------|------------------------------|-----------------------------------|-----------------------------------|------------------------------|------------------|
| 202223      | Financial year   | School            | E92000001    | England      | 822         | E06000055    | Bedford | 10074571     | 109464     | 8222064         | Balliol Primary School | Community school | Primary      | z     | No      | 1144896                   | 0                      | 0                      | 1144896                      | 46952       | 63852        | 21062        | 1967         | 48076        | 0            | 0            | 0            | 71105        | 181909                    | 0                   | 34348              | 0                     | 188464                             | 127000                | 0                      | 0                | 0                        | 32768                              | 0                   | 0                                  | 0                           | 1709385                       | 0                           | 1709385                                | 83831           | 343                     | 4983.63                 | 139885             | 101                   | 27112                                      | 18970               | 297                        | 14645                                    | 15228                          | 47565                      | 1972790        |
| 202223      | Financial year   | School            | E92000001    | England      | 822         | E06000055    | Bedford | 10029936     | 136085     | 8226905         | Bedford Academy       | Academy sponsor led | Secondary    | HEART ACADEMIES TRUST | Yes       | 0      | 3172150                   | 2084511                | 5256661                | 164830                         | 353617      | 103260       | 5733         | 193851       | 66768        | 53747        | 0            | 423359       | 941806       | 0                           | 55719               | 0                   | 695481                | 127000                             | 0                     | 0                      | 0                | 0                        | 0                                  | 0                   | 0                                  | 0                           | 7076667                       | 0                           | 7076667                                | 353833          | 1067                    | 6632.3                  | 383165             | 389                   | 0                                         | x                   | x                          | x                                       | 107364                          | 64638                          | 215302         |
| ...         | ...              | ...               | ...          | ...          | ...         | ...         | ...     | ...          | ...        | ...             | ...         | ...          | ...          | ...   | ...     | ...                       | ...                    | ...                    | ...                            | ...         | ...          | ...          | ...          | ...          | ...          | ...          | ...          | ...                         | ...                 | ...                 | ...                   | ...                                | ...                   | ...                    | ...              | ...                     | ...                                  | ...               | ...                                  | ...                         | ...                               | ...                         | ...                                  | ...             | ...                     | ...                     | ...                  | ...                      | ...                                        | ...                  | ...                          | ...                                   | ...                                   | ...                          | ...              |

In this un-normalized form, all the data is stored in a single table, resulting in redundant information and potential data integrity issues. Each row represents a school with various attributes, and the data is not organized efficiently, leading to data duplication and inconsistency. Normalization helps address these issues by organizing the data into smaller, related tables, improving efficiency and reducing redundancy.

## Answer 2

In the first normal form (1NF), the data is organized into separate tables, and each table contains only atomic (indivisible) values. There are no repeating groups or arrays within a table. Here are examples of definitions for each relation in 1NF:

**Schools Table:**

| school_ukprn | school_urn | school_laestab | school_name | school_type | school_phase | trust | academy | ... (other columns) ... |
|--------------|------------|-----------------|-------------|-------------|--------------|-------|---------|---------------------------|
| 10074571     | 109464     | 8222064         | Balliol Primary School | Community school | Primary | Yes | No | ... (other data) ... |
| 10029936     | 136085     | 8226905         | Bedford Academy | Academy sponsor led | Secondary | HEART ACADEMIES TRUST | Yes | ... (other data) ... |
| ...          | ...        | ...             | ...         | ...         | ...          | ...   | ...     | ...                       |

**Funding Table:**

| school_ukprn | basic_entitlement_primary | basic_entitlement_ks3 | basic_entitlement_ks4 | ... (other columns) ... |
|--------------|--------------------------|-----------------------|-----------------------|-------------------------|
| 10074571     | 1144896                  | 0                     | 0                     | ... (other data) ... |
| 10029936     | 3172150                  | 2084511               | 5256661               | ... (other data) ... |
| ...          | ...                      | ...                   | ...                   | ...                     |

In this 1NF representation:

1. **Atomic Values:** Each column in the tables contains atomic values. For example, the `school_type` column in the Schools table contains only singular, indivisible values like "Community school" or "Academy sponsor led".

2. **No Repeating Groups:** There are no repeating groups or arrays within the tables. Each column contains data of the same type, and there are no nested structures.

3. **Unique Identifiers:** Each table has a unique identifier, like `school_ukprn`, ensuring that each row in the table is uniquely identifiable.

This representation is in 1NF because it meets the basic requirements of having atomic values and organizing the data into separate tables without repeating groups.


## Answer 3

To transform the data from the first normal form (1NF) to the second normal form (2NF) and potentially to the third normal form (3NF), we need to eliminate partial and transitive dependencies in the tables. In the given data, there seems to be a composite primary key comprising `school_ukprn` and `time_period`, and based on this assumption, let's proceed with the normalization process.

**Step 1: Identify Partial Dependencies and Separate Tables**

From the provided data, it appears that columns such as `time_period`, `time_identifier`, and other non-key attributes are fully functionally dependent on the composite primary key `(school_ukprn, time_period)`. We can create separate tables to remove partial dependencies.

**Schools Table (2NF):**

| school_ukprn | school_name | school_type | school_phase | trust | academy |
|--------------|-------------|-------------|--------------|-------|---------|
| 10074571     | Balliol Primary School | Community school | Primary | Yes | No |
| 10029936     | Bedford Academy | Academy sponsor led | Secondary | HEART ACADEMIES TRUST | Yes |
| ...          | ...         | ...         | ...          | ...   | ...     |

**Time Period Table (2NF):**

| school_ukprn | time_period | time_identifier |
|--------------|-------------|-----------------|
| 10074571     | 202223      | Financial year |
| 10029936     | 202223      | Financial year |
| ...          | ...         | ...             |

**Funding Table (2NF):**

| school_ukprn | basic_entitlement_primary | basic_entitlement_ks3 | basic_entitlement_ks4 | ... (other columns) ... |
|--------------|--------------------------|-----------------------|-----------------------|-------------------------|
| 10074571     | 1144896                  | 0                     | 0                     | ... (other data) ... |
| 10029936     | 3172150                  | 2084511               | 5256661               | ... (other data) ... |
| ...          | ...                      | ...                   | ...                   | ...                     |

**Step 2: Remove Transitive Dependencies**

From the given data, it seems that columns like `school_type`, `school_phase`, `trust`, and `academy` are fully functionally dependent on `school_ukprn`. Therefore, we can create a separate table for these attributes to remove transitive dependencies.

**School Details Table (3NF):**

| school_ukprn | school_type | school_phase | trust | academy |
|--------------|-------------|--------------|-------|---------|
| 10074571     | Community school | Primary | Yes | No |
| 10029936     | Academy sponsor led | Secondary | HEART ACADEMIES TRUST | Yes |
| ...          | ...         | ...          | ...   | ...     |

In this 3NF representation, we have eliminated partial and transitive dependencies, resulting in separate tables that adhere to the second and third normal forms. Each table has a clear primary key and contains non-key attributes that are fully functionally dependent on the respective primary key.
