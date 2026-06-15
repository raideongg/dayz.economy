# Changelog

Version numbers mirror DayZ releases. MAJOR.MINOR corresponds to the DayZ game version (currently 1.29), while PATCH represents our revision of the Central Economy files (1.29.1, 1.29.2, etc.). A new DayZ release advances the version (for example, 1.30.0).

## [1.29.2] - 2026-06-14

### Removed

#### `ChristmasTree` & `ChristmasTree_Green`
Temporarily removed references to `ChristmasTree` and `ChristmasTree_Green` from all map files. These types currently generate console errors indicating that they are not spawnable, likely due to a non-public scope. Because they are only used by holiday events, they can be safely removed for the time being and will be restored once the underlying issue has been resolved.

This change impacts the following files:
- `db/events.xml`, `db/types.xml`, `cfgeventspawns.xml`, `mapgroupproto.xml`

#### `ShippingContainerKeys_Red`
Corrected several issues with the `ShippingContainerKeys_Red` type on Chernarus and Livonia, including incorrect `<lifetime>`, `<restock>`, `<category>`, and `<usage>` values. Removed the invalid `<value name="Tier4"/>` entry, which generated an error on Livonia because the map does not include a `Tier4` definition.

---

## [1.29.1] - 2026-06-14

This release introduces a significant number of changes intended to address both well-known and lesser-known issues in the vanilla [DayZ Central Economy](https://github.com/BohemiaInteractive/DayZ-Central-Economy) files for Chernarus, Livonia, and Sakhal.

These files are designed as a drop-in replacement for DayZ PC servers and are derived directly from the vanilla DayZ Central Economy files, with no departures from the core vanilla foundation beyond required patches.