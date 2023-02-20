# Sorting Algorithms

![](https://sp-ao.shortpixel.ai/client/to_avif,q_glossy,ret_img,w_750/https://simplesnippets.tech/wp-content/uploads/2019/07/bubble-sort-sorting-algorithm.jpg)

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQE2x8GeiLD2O8kQMi_nu59o69xACZT2MhPuw&usqp=CAU)

## General

- Allowed editors: `vi`, `vim`, `emacs`
- All your files will be compiled on `Ubuntu 20.04` LTS using `gcc`, using the options `-Wall` `-Werror` `-Wextra` `-pedantic` `-std=gnu89`
- All your files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the Betty style. It will be checked using `betty-style.pl` and `betty-doc.pl`
- You are not allowed to use global variables
- No more than 5 functions per file
- Unless specified otherwise, you are not allowed to use the standard library. Any use of functions like `printf`, `puts`, … is totally forbidden.
- The prototypes of all your functions should be included in your header file called `sort.h`
	_Don’t forget to push your header file_
- All your header files should be include guarded
- A list/array does not need to be sorted if its size is less than 2.

## AIM :sunflower:
- At least four different sorting algorithms
- What is the Big O notation, and how to evaluate the time complexity of an algorithm
- How to select the best sorting algorithm for a given input
- What is a stable sorting algorithm


Data Structure:
```
typedef struct listint_s
{
	const int n;
	struct listint_s *prev;
	struct listint_s *next;
} listint_t;
```

Function Prototypes:

| File                       | Prototype                                         |
| -------------------------- | ------------------------------------------------- |
| `print_array.c`            | `void print_array(const int *array, size_t size)` |
| `print_list.c`             | `void print_list(const listint_t *list)`          |
| `0-bubble_sort.c`          | `void bubble_sort(int *array, size_t size);`      |
| `1-insertion_sort_list.c`  | `void insertion_sort_list(listint_t **list);`     |
| `2-selection-sort.c`       | `void selection_sort(int *array, size_t size);`   |
| `3-quick_sort.c`           | `void quick_sort(int *array, size_t size);`       |
| `100-shell_sort.c`         | `void shell_sort(int *array, size_t size);`       |
| `101-cocktail_sort_list.c` | `void cocktail_sort_list(listint_t **list);`      |
| `102-counting_sort.c`      | `void counting_sort(int *array, size_t size);`    |
| `103-merge_sort.c`         | `void merge_sort(int *array, size_t size);`       |
| `104-heap_sort.c`          | `void heap_sort(int *array, size_t size);`        |
| `105-radix_sort.c`         | `void radix_sort(int *array, size_t size);`       |
| `106-bitonic_sort.c`       | `void bitonic_sort(int *array, size_t size);`     |
| `107-quick_sort_hoare.c`   | `void quick_sort_hoare(int *array, size_t size);` |



Data Structures:
```
typedef enum kind_e
{
	SPADE = 0,
	HEART,
	CLUB,
	DIAMOND
} kind_t;
typedef struct card_s
{
	const char *value;
	const kind_t kind;
} card_t;
typedef struct deck_node_s
{
	const card_t *card;
	struct deck_node_s *prev;
	struct deck_node_s *next;
} deck_node_t;
```

Function Prototype:

| File               | Prototype                             |
| ------------------ | ------------------------------------- |
| `1000-deck_node.c` | `void sort_deck(deck_node_t **deck);` |
