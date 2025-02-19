## Unreleased

### Added
* Update ServiceResaleItem record fields/record refs for 2021.2. `item_options_list`, `presentation_item_list`, `site_category_list`, `translations_list` were all removed as fields as the are not simple fields, they require special classes. (#500)
* Dependabot to CI
* CI run for Ruby 3
* Add CI run for an environment with and without `tzinfo` installed
* Update NonInventorySaleItem record fields/record refs for 2021.2. `item_options_list`, `presentation_item_list`, `product_feed_list`, `site_category_list`, `translations_list` were all removed as fields as the are not simple fields, they require special classes. (#503)
* Implement MatrixOptionList#to_record (#504)
* Update ItemVendor record fields/record refs for 2021.1. `vendor` is now a record_ref instead of a field. (#505)
* Update InventoryItem record fields/record refs for 2021.2. `member_list` was removed as a field as it doesn't belong to InventoryItem. (#506)
* Update LotNumberedInventoryItem record fields/record refs for 2021.2. (#507)
* Update NonInventoryResaleItem record fields/record refs for 2021.2. `item_options_list`, `presentation_item_list`, `product_feed_list`, `site_category_list`, `translations_list` were all removed as fields as the are not simple fields, they require special classes. (#508)
* Add `attach_file` action for Invoice and SalesOrder. (#509)
* Add ItemOptionCustomField recrd (#512)

### Fixed
* Fix "undefined method `[]` for #<Nori::StringIOFile>" when adding File (#495)
* Moved definition of `search_joins` attribute from records to search action. The attribute was removed for AssemblyComponent, SerializedInventoryItemLocation, and WorkOrderItem as they don't offer the search action. (#511)

## 0.8.10

### Added

* Update Estimate record fields/record refs for 2021.2. `balance`, `bill_address`, `bill_is_residential`, and `is_multi_ship_to` were all removed as fields as either being incorrect, outdated, or a search-only field. (#496)

### Fixed

* Savon 2.12 supported

## 0.8.9

### Fixed

* Fixed issue where search only fields could be specified when an existing field exists. https://github.com/NetSweet/netsuite/pull/488

## 0.8.8

### Added

* Adding serialized assembly item to get_item
* Add CostCategory record (#482)
* Introduce search only fields (#483)

### Fixed

* Fix accessing custom field values returned in advanced search results (#480)
* Fixing bug where single-selection custom multi select fields would incorrectly be parsed 3377c971d0cb727d81f4b4bc6e30edfbdfaccfd1
* Fixed some field definitions on serialized assembly item
* Properly extract external_id from advanced search results (#478)
