---
{"dg-publish":true,"permalink":"/development/dataview-bookshelf/","hide":true,"tags":["type/tutorial"],"created":"2024-12-15T09:21:56.920+01:00","updated":"2024-12-17T23:12:39.394+01:00"}
---



# Example


| File                                                        | Cover                                                                                                                                     | Author        |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| [[5_Books/Oliver Heaviside\|Oliver Heaviside]]           | ![Oliver Heaviside](http://books.google.com/books/content?id=e9wEntQmA0IC&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api)      | Paul J. Nahin |
| [[5_Books/The View From Nowhere\|The View From Nowhere]] | ![The View From Nowhere](http://books.google.com/books/content?id=5cryOCGb2nEC&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api) | Thomas Nagel  |
| [[5_Books/We Are Electric\|We Are Electric]]             | ![We Are Electric](http://books.google.com/books/content?id=zQZ_EAAAQBAJ&printsec=frontcover&img=1&zoom=1&edge=curl&source=gbs_api)       | Sally Adee    |

{ .block-language-dataview}


# Grammar

```
TABLE 
book_cover as Cover,
book_author as Author
FROM "5_Books" AND #type/book
LIMIT 3
SORT file.name ASC
```

## 1. TABLE

```
TABLE 
```
 

- Defines the output format for the query. In this case, TABLE keyword specifies that the results will be displayed in a tabular form.

## 2. Column definitions

```
book_cover as Cover,
book_author as Author
```

### Syntax

Each filed (`book_cover`, `book_author`) is followed by the column name (`Cover`, `Author`).

### Field

- `book_cover` and `book_author` refer to the property defined in the notes.


# 3. Source

```
FROM "5_Books" AND #type/book
```

It specifies the source of the data.

1. **Folder Restriction**: `"5_Books"` specifies that the query searches for notes within the folder named `5_Books`.
2. **Tag Filtering**: `#type/book` further filters notes to include only those tagged with `#type/book`.


# 4. Limit

```
LIMIT 3
```

Limit the number of rows.

# 5. Sort

```
SORT file.name ASC
```

- Orders the results in the table.
- **Components**:
    - `file.name`: Refers to the name of the file (note).
    - `ASC`: Specifies ascending order.
        - Alternative: Use `DESC` for descending order.


# References

https://s-blu.github.io/obsidian_dataview_example_vault/