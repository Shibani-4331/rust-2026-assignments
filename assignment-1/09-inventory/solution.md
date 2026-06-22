# Solution notes: Inventory

## Approach

'summary' borrows the inventory slice, counts the number of entries, and sums all quantities to produce a formatted string. 
'restock' consumes both inventory vectors and merges items with the same name by accumulating quantities in a HashMap. 
The final inventory is produced from the map entries.

## Edge cases handled
Empty inventories.
Items that appear in only one inventory.
Items that appear multiple times across both inventories.
Quantities are added together for matching item names.

## Anything special

summary takes a shared reference and does not consume the inventory, allowing the inventory to be used afterward. 
restock takes ownership of both vectors, allowing item names (String) to be moved directly into the merged inventory without cloning.