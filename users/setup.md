# Before You Start

Before you start using TEC-RFID Asset, it's a good idea to plan out how you want to structure your data--this will help prevent you from having to spend lots of time updating existing assets later on. No two setups are going to look alike--it depends entirely on what it is you're tracking and what you want to do with the data. 

This is a broad-strokes summary: if you would like further detailed setup guidance, we'd be happy to help! 

 - What are your goals?
   - Knowing what success looks like to you heavily influences how you configure your tracking system.
   - Think about the sort of information you'd like to have at your fingertips when you scan an asset. What would you like to be able to see--or to update?
   - Do you want to export data to other locations or integrate with other apps?
 - Who are your users going to be?
   - What sort of information will each of your staff members need?
   - What level of access will they require?
   - You'll want at least two people to have full admin access so you have a backup in case of staff absence. 
 - What locations will you need to list?
   - What areas are you going to want to stocktake? How specific do you want to get? 
   - Aim for a good balance between specific and vague: a cabinet, for example, rather than a whole room or a single shelf. 
   - You can nest locations inside each other (but note that stocktakes will not search sublocations). 
   - If you have an existing warehouse labelling system, it'll likely make sense to carry that over.
   - Locations don’t have to be a single fixed physical location—they could be a van, for instance, or a tool bag.
 - What categories / asset groups will you need?
   - Both are used to sort assets, but with key differences. You can use one, both, or neither. Assets can belong to both a group and a category.
   - Categories are usually going to be your first choice for asset organisation. You can use them to filter stocktakes, and they can be nested inside each other.
   - Asset groups are useful if you need to do additional filtering that doesn't fit into your category structure. They are not used for filtering stocktakes and they cannot be nested. 
   - Example: an IT department tracking equipment might use asset groups for equipment type--monitors, laptops, phones, etc--and categories for the department they're assigned to--accounting, sales, marketing, etc. This would allow them to easily stocktake a single department's equipment while still separating the assets into their physical types for their records.
 - What asset types / custom fields will you need?
   - You can create any kind of custom field you need: text, numbers, dropdown menus, etc. You can also customise which of the default system fields you would like to use. 
   - An 'asset type' is essentially a template for different kinds of assets: you can assign different custom fields to different types, allowing you to store different data about different kinds of assets.

# Set Up

You can create new Locations, Categories, Asset Groups, or Asset Types by selecting the relevant module in the sidebar and clicking + CREATE NEW. 

If you have too many to easily add manually, an import function is available: just click IMPORT, download the template, make your edits in Excel or your preferred spreadsheet app, and upload your document. 

## Categories

(Under Assets in the sidebar.)

Creating and editing these is pretty straightforward: create your top level category first, then create your child category/ies and select the parent category from the dropdown. 

## Asset Groups

(Under Assets in the sidebar.)

These only require a title and a description--unlike categories, there's no nesting. 

## Asset Types

(Under Assets in the sidebar.)

These only require a title and a description--the custom field assignment is done in Settings. 

## Locations

Creating and editing these is pretty straightforward: create your top level location first, then create your child location(s) and select the parent location from the dropdown. You can also, optionally, record the location's address. 

For details on how to manage fixed readers, [click here](https://github.com/TEC-RFID/rfid-asset-documentation/blob/main/users/fixedreaders.md). 

## Settings

### Asset Fields

Here you can hide the default system asset fields you don't need, mark them as mandatory if necessary*, and restrict edit access to certain user roles. You can also click and drag the fields to reorder them. 

### Custom Fields

 - Field names have to contain at least one letter of the alphabet (so not just numbers).
 - Available element types:
   - Text box (can be restricted to numbers, emails, URLs, or dates, or be any format)
   - Textarea (larger text box)
   - List box (dropdown menu)
   - Checkbox(es) (can select multiple options)
   - Radio buttons (can select only one option)
  - For the field types with options (list boxes, checkboxes, radio buttons), fill in the options in the Field Value box, with one option on each line.
  - Assign it to a specific asset type by choosing an option from the dropdown; or, if you want it to appear on all assets regardless of type, tick 'is global field'.
  - To make the field mandatory*, tick 'is required field'.

* A note on mandatory fields: we suggest using these sparingly--only use them in situations where the user will always have the required information to fill in the field. Otherwise, you tend to end up with nonsense data.

### User Roles

t
