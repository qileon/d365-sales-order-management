# Project Scope

## Included

This repository includes the main SOrder feature set:

- Custom sales order header and line tables
- Order parameter table and form
- Sales order form and list part
- Service classes for approval, cancellation, validation, and recalculation
- Number sequence related EDT and module extension
- Order status enum
- Data entities and staging tables
- Menu items and module menu metadata
- Security role, duties, and privileges
- Test classes from the training project
- Label metadata and English label resources

## Included Dependencies

These files are included because the SOrder artifacts reference them directly:

- `SOrderID.xml`
- `SOrderNumberSequence.xml`
- `SOrderStatus.xml`
- `SLabels_en-US.xml`
- `SLabels.en-US.label.txt`
- `SNumberSeqModule.xml`
- `NumberSeqModule.Tiryaki1.xml`
- SOrder menu items
- SOrder security artifacts
- SOrder data entities and staging tables

## Excluded From This Repository

The following areas are outside the scope of this repository:

- ITM inventory tables, forms, reports, batch jobs, and tiles
- ITM stock movement reporting artifacts
- ITM warehouse stock synchronization logic
- SalesLine/SalesTable extensions that belong to the inventory integration repo

The original internship project combined order management and inventory management in one D365 model. This repository focuses on the SOrder module so the order management foundation can be reviewed separately from the later inventory features.

## Related Work

The inventory module is documented separately in the `d365-inventory-stock-management` repository. That project focuses on warehouse stock tracking, stock movement logging, low stock checks, SSRS reporting, and order integration.

## Design Reflections

This project is preserved as an internship project snapshot rather than an actively maintained product. If the same module were designed again in a longer term environment, the main engineering considerations would be:

- Clearer separation between order management and inventory integration
- More complete automated test coverage
- Stronger validation coverage around state transitions
- More detailed setup documentation for number sequences and security
- More explicit import/export examples for the data entities
