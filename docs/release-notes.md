[Back To Home](index.md)

# Release Notes

## 0.7 December 2023

- Updated all metadata to v59.0
- Modified firmworks__Nearby_Setting__mdt from Package Protected to public
- Modified Permission Sets to include Custom Metadata
- Introduced Interop - Component Group Alias
  - Because the search, list and map components work via client side events - adding multiple components (via tabs or other layout) resulted in inconsistant behavior.
  - The design time configuration can be set with a unique arbitrary custom value so that the search/list/map and other components can subscribe to the same group that have the same setting.
- List component now can show a driving directions button which can be turned on/off in design - this feature opens a google.com directions screen for the first 23 addresses in the list component. The url can be subsequently shared to a phone for drive navigation.
- List component can now hide the download button
- Introduced contextId in search - If adding the search component to a record layout - a filter can be set to provide subsets
  - for example the search component can be added to an account layout, it can be configured to show a contacts map and list
  - Create a filter on the Contacts Mailing Configuration - Add '(AccountId = :contextId)'
  - From within the configuration for the search component on the account layout - set the default filter list and set the filter to the one you created


## 0.5 August 2023

- Rebrand from "Nearby" to "FirmWorks Geo"

## 0.3 May 2023

### Enhancement

- Map component and List components can now be placed in tabs or other deferred rendering sections aiding with dynamic and smaller page layouts.

## 0.2 May 2023

### fixes

- Support for specifying parent relationships in configuration screen
- Minor fix for using Geo fields on a page layout

## 0.1 January 2023

- FirmWorks Geo application supports
  - Multiple ways to set searching from
    - Built in Geo Encoding using full address
    - Support for Google API key
    - Using device location
    - Record based from layout
  - List of results with download as CSV option
  - Graphical map showing multiple markers
- Extensible support for contextual record selection for custom LWC and Aura components
