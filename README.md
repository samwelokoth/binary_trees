# C - Trees in Binary Form

Our collaborative endeavor delved into the intricacies, merits, and drawbacks associated with utilizing trees as fundamental data structures. We acquired insights into tree categorization and traversal techniques. Over the course of our project, we implemented various types of binary trees including binary, binary search, AVL, and Max Binary Heap.

## Verification of Implementations :heavy_check_mark:

* [tests](./tests): Collection of test files for comprehensive assessment. Supplied by ALX.

## Facilitative Resource :raised_hands:

* [binary_tree_print.c](./binary_tree_print.c): C module facilitating the visually appealing printing of binary trees.

## Header Definitions :file_folder:

* [binary_trees.h](./binary_trees.h): Header file housing essential definitions and function prototypes indispensable for the project.

Data Structures
```
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;
typedef struct binary_tree_s bst_t;
typedef struct binary_tree_s avl_t;
typedef struct binary_tree_s heap_t;
```

Function Prototypes

| File                             | Prototype                                                                                        |
| -------------------------------- | ------------------------------------------------------------------------------------------------ |
| `binary_tree_print.c`            | `void binary_tree_print(const binary_tree_t *tree)`                                              |
| `0-binary_tree_node.c`           | `binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);`                             |
| `1-binary_tree_insert_left.c`    | `binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);`                      |
| `2-binary_tree_insert_right.c`   | `binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);`                     |
| `3-binary_tree_delete.c`         | `void binary_tree_delete(binary_tree_t *tree);`                                                  |
| `4-binary_tree_is_leaf.c`        | `int binary_tree_is_leaf(const binary_tree_t *node);`                                            |
| `5-binary_tree_is_root.c`        | `int binary_tree_is_root(const binary_tree_t *node);`                                            |
| `6-binary_tree_preorder.c`       | `void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));`                       |
| `7-binary_tree_inorder.c`        | `void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));`                        |
| `8-binary_tree_postorder.c`      | `void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));`                      |
| `9-binary_tree_height.c`         | `size_t binary_tree_height(const binary_tree_t *tree);`                                          |
| `10-binary_tree_depth.c`         | `size_t binary_tree_depth(const binary_tree_t *tree);`                                           |
| `11-binary_tree_size.c`          | `size_t binary_tree_size(const binary_tree_t *tree);`                                            |
| `12-binary_tree_leaves.c`        | `size_t binary_tree_leaves(const binary_tree_t *tree);`                                          |
| `13-binary_tree_nodes.c`         | `size_t binary_tree_nodes(const binary_tree_t *tree);`                                           |
| `14-binary_tree_balance.c`       | `int binary_tree_balance(const binary_tree_t *tree);`                                            |
| `15-binary_tree_is_full.c`       | `int binary_tree_is_full(const binary_tree_t *tree);`                                            |
| `16-binary_tree_is_perfect.c`    | `int binary_tree_is_perfect(const binary_tree_t *tree);`                                         |
| `17-binary_tree_sibling.c`       | `binary_tree_t *binary_tree_sibling(binary_tree_t *node);`                                       |
| `18-binary_tree_uncle.c`         | `binary_tree_t *binary_tree_uncle(binary_tree_t *node);`                                         |
| `100-binary_trees_ancestor.c`    | `binary_tree_t *binary_trees_ancestor(const binary_tree_t *first, const binary_tree_t *second);` |
| `101-binary_tree_levelorder.c`   | `void binary_tree_levelorder(const binary_tree_t *tree, void (*func)(int));`                     |
| `102-binary_tree_is_complete.c`  | `int binary_tree_is_complete(const binary_tree_t *tree);`                                        |
| `103-binary_tree_rotate_left.c`  | `binary_tree_t *binary_tree_rotate_left(binary_tree_t *tree);`                                   |
| `104-binary_tree_rotate_right.c` | `binary_tree_t *binary_tree_rotate_right(binary_tree_t *tree);`                                  |
| `110-binary_tree_is_bst.c`       | `int binary_tree_is_bst(const binary_tree_t *tree);`                                             |
| `111-bst_insert.c`               | `bst_t *bst_insert(bst_t **tree, int value);`                                                    |
| `112-array_to_bst.c`             | `bst_t *array_to_bst(int *array, size_t size);`                                                  |
| `113-bst_search.c`               | `bst_t *bst_search(const bst_t *tree, int value);`                                               |
| `114-bst_remove.c`               | `bst_t *bst_remove(bst_t *root, int value);`                                                     |
| `120-binary_tree_is_avl.c`       | `int binary_tree_is_avl(const binary_tree_t *tree);`                                             |
| `121-avl_insert.c`               | `avl_t *avl_insert(avl_t **tree, int value);`                                                    |
| `122-array_to_avl.c`             | `avl_t *array_to_avl(int *array, size_t size);`                                                  |

## Undertakings :page_with_curl:

* **0. Novel Node Creation**
  * [0-binary_tree_node.c](./0-binary_tree_node.c): C functionality devised to fashion a
  binary tree node furnished with a specified parent and value.
  * Proffers a pointer denoting the freshly formed node, or `NULL` upon failure.

* **1. Embedding on the Left**
  * [1-binary_tree_insert](./1-binary_tree_insert): C procedure engineered to integrate a
  node as the left progeny of another.
  * Yields a pointer signifying the recent node, or `NULL` in case of failure.
  * If the designated `parent` already encompasses a left node, the recent node assumes its
  position while the erstwhile left progeny metamorphoses into the left progeny of the new node.

* **2. Embedding on the Right**
  * [2-binary_tree_insert_right.c](./2-binary_tree_insert_right.c): C operation tailored for the
  embedding of a node as the right progeny of another.
  * Dispenses a pointer designating the novel node, or `NULL` in the event of failure.
  * In the scenario where the provided `parent` already houses a right node, the novel node
  assumes its place and the previous right progeny transitions into the right progeny of the novel node.

* **3. Obliteration**
  * [3-binary_tree_delete.c](./3-binary_tree_delete.c): C mechanism devised for the eradication
  of an entire binary tree.

* **4. Determin

ing Leaf Status**
  * [4-binary_tree_is_leaf.c](./4-binary_tree_is_leaf.c): C module engineered to ascertain
  whether a given node constitutes a leaf.
  * Furnishes `1` upon confirming leaf status, and `0` otherwise.

* **5. Root Verification**
  * [5-binary_tree_is_root.c](./5-binary_tree_is_root.c): C function architected to validate
  if a given node serves as the root.
  * Conveys `1` to denote root status, and `0` otherwise.

* **6. Traversal in Pre-order**
  * [6-binary_tree_preorder.c](./6-binary_tree_preorder.c): C function crafted to navigate
  a tree via pre-order traversal.

* **7. Traversal in In-order**
  * [7-binary_tree_inorder.c](./7-binary_tree_inorder.c): C function contrived for traversing
  a tree employing in-order traversal.

* **8. Traversal in Post-order**
  * [8-binary_tree_postorder.c](./8-binary_tree_postorder.c): C function formulated for traversing
  a tree utilizing post-order traversal.

* **9. Ascertainment of Height**
  * [9-binary_tree_height.c](./9-binary_tree_height.c): C functionality engineered to ascertain
  the height of a binary tree.

* **10. Gauge of Depth**
  * [10-binary_tree_depth.c](./10-binary_tree_depth.c): C function devised to compute
  the depth of a designated node within a binary tree.

* **11. Size Measurement**
  * [11-binary_tree_size.c](./11-binary_tree_size.c): C mechanism concocted to determine
  the size of a binary tree.

* **12. Quantification of Leaves**
  * [12-binary_tree_leaves.c](./12-binary_tree_leaves.c): C operation crafted to enumerate
  the quantity of leaves in a binary tree.

* **13. Enumeration of Nodes**
  * [13-binary_tree_nodes.c](./13-binary_tree_nodes.c): C module designed to enumerate
  the quantity of nodes in a binary tree possessing at least one child.

* **14. Evaluation of Balance Factor**
  * [14-binary_tree_balance.c](./14-binary_tree_balance.c): C function formulated to evaluate
  the balance factor of a binary tree.

* **15. Integrity Assessment**
  * [15-binary_tree_is_full.c](./15-binary_tree_is_full.c): C procedure engineered to scrutinize
  the integrity of a binary tree.
  * Renders `1` to affirm tree integrity, and `0` otherwise.

* **16. Perfection Evaluation**
  * [16-binary_tree_is_perfect.c](./16-binary_tree_is_perfect.c): C functionality tailored for
  evaluating the perfection of a binary tree.
  * Returns `1` to indicate tree perfection, and `0` otherwise.

* **17. Sibling Identification**
  * [17-binary_tree_sibling.c](./17-binary_tree_sibling.c): C operation devised to pinpoint
  a pointer to the sibling of a specified node within a binary tree.
  * Dispenses `NULL` in the absence of a sibling.

* **18. Uncle Identification**
  * [18-binary_tree_uncle.c](./18-binary_tree_uncle.c): C function contrived to discern
  a pointer to the uncle of a specified node within a binary tree.
  * Conveys `NULL` if no uncle is discerned.

* **19. Determination of Lowest Common Ancestor**
  * [100-binary_trees_ancestor.c](./100-binary_trees_ancestor.c): C procedure devised for
  identifying a pointer to the lowest common ancestor node of two designated nodes within a binary tree.
  * Delivers `NULL` in the absence of a common ancestor.

* **20. Traversal in Level-order**
  * [101-binary_tree_levelorder.c](./101-binary_tree_levelorder.c): C function contrived for
  traversing a binary tree via level-order traversal.

* **21. Completeness Verification**
  * [102-binary_tree_is_complete.c](./102-binary_tree_is_complete.c): C function architected to
  validate the completeness of a binary tree.
  * Conveys `1` to denote tree completeness, and `0` otherwise.

* **22. Left Rotation**
  * [103-binary_tree_rotate_left.c](./103-binary_tree_rotate_left.c): C mechanism devised to execute
  a left rotation on a binary tree.
  * Returns a pointer to the fresh root node of the tree post-rotation.

* **23. Right Rotation**
  * [104-binary_tree_rotate_right.c](./104-binary_tree_rotate_right.c): C functionality tailored to
  enact a right rotation on a binary tree.
  * Dispenses a pointer to the novel root node of the tree post-rotation.

* **24. Validation of BST**
  * [110-binary_tree_is_bst.c](./110-binary_tree_is_bst.c): C operation crafted for verifying
  if a binary tree manifests as a valid binary search tree.
  * Conveys `1` to indicate a valid BST, and `0` otherwise.

* **25. Incorporation into BST**
  * [111-bst_insert.c](./111-bst_insert.c): C procedure contrived for integrating a value into
  a binary search tree.
  * Furnishes a pointer to the new node, or `NULL` upon failure.
  * In the event the tree is devoid of nodes, the value becomes the root node.
  * The value is disregarded if already existing in the tree.

* **26. Array to BST Transformation**
  * [112-array_to_bst.c](./112-array_to_bst.c): C function engineered to transform an array into
  a binary search tree.
  * Yields a pointer to the root node of the resultant tree, or `NULL` upon failure.

* **27. BST Search**
  * [113-bst_search.c](./113-bst_search.c): C operation devised for searching a value within
  a binary search tree.
  * Returns a pointer to the matched node if the value is found within the BST.
  * Otherwise, dispenses `NULL`.

* **28. BST Node Removal**
  * [114-bst_remove.c](./114-bst_remove.c): C mechanism tailored for eliminating a node from
  a binary search tree.
  * Yields a pointer to the fresh root node of the tree post-deletion.
  * In the scenario where the node to be eradicated harbors two children, it gets substituted with its
  initial in-order successor.

* **29. Big O Analysis on BST**
  * [115-O](./115-O): Document encapsulating the average time complexities pertinent to
  binary search tree operations (each answer delineated on a separate line):
    * Insertion of the value `n`.
    * Removal of the node carrying the value `n`.
    * Search for a node within a BST of magnitude `n`.

* **30. AVL Validity Assessment**
  * [120-binary_tree_is_avl.c](./120-binary_tree_is_avl.c): C functionality crafted for evaluating
  if a binary tree qualifies as a valid AVL tree.
  * Conveys `1` to denote a valid AVL tree, and `0



Authors:
This project was done by Samwel OKoth
You can reach me via :
gmail:samwelokoth8@gmail.com
