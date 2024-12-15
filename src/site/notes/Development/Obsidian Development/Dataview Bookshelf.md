---
{"dg-publish":true,"dg-path":"Development/Obsidian","permalink":"/development/obsidian/","tags":["type/tutorial","status/done"],"dgShowToc":true,"created":"2024-12-15T09:21:56.920+01:00","updated":"2024-12-15T11:33:54.726+01:00"}
---


# Example


| File                                                                            | Cover                                                                   | Author               |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | -------------------- |
| [[5_Books/Epistemic Injustice\|Epistemic Injustice]]                         | ![[5_Books/_media/Bookcovers/Epistemic Injustice.jpg\|100]]             | Miranda Fricker      |
| [[5_Books/Oliver Heaviside\|Oliver Heaviside]]                               | ![[5_Books/_media/Bookcovers/Oliver Heaviside.jpg\|100]]                | Paul J. Nahin        |
| [[5_Books/The Companion Species Manifesto\|The Companion Species Manifesto]] | ![[5_Books/_media/Bookcovers/The Companion Species Manifesto.jpg\|100]] | Donna Jeanne Haraway |

{ .block-language-dataview}


# Grammar

```
TABLE 
book_cover as Cover,
book_author as Author
FROM "5_Books" AND #type/book
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


# 4. Sort

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