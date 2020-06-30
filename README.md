# project-cours-Data-structures-and-algorithms
Explanation -
This data structure consists of the following structures:
1. Two black red trees, one for the subscriptions and the other for the books.
Each node in the subscription tree contains: key, node color, father and son pointers, array size 10 (inclusion of 10) pointers to book nodes, subscription name, maximum number of books, current book number, and pointer to the corresponding vertex in a two-way linked list.
The array will henceforth be called - the array of books, at the subscription node or a pointer array of books, at the subscription node.
Each node in the book tree contains: key, node color, pointer to father and son, and pointer to subscriber node which
Lends the book.
The tree that contains the subscriptions will henceforth be called - the subscription tree.
The tree containing the books will henceforth be called the book tree.

2. An 11-cell array, each cell containing a two-way linked list.
This structure is intended primarily for the query, which requests all subscribers who lend the most number of books. For each subscription there is a vertex, contained in the linked list, indexed in the array, which is the number of books borrowed by it.

That is, if Roy lent 2 books, then for him there is a vertex in the linked list in index 2, in the above array. If Roy returns his vertex book to the linked list in index 0 and if lent another book.
The insertion and deletion actions from a list are permanent because it is bidirectional.

The vertex of the linked list is monotonous, it is created when you subscribe to the data structure, accompanied
It is maintained throughout the subscription period and is only deleted when the subscription is deleted from the structure.
The vertex and the subscription node contain reciprocal pointers.
This array will henceforth be called - the structure array, as it is the only array contained in the structure level, along with
The trees.
(Do not get confused with the array contained in the subscription node, which will be the array of books at the subscription node).
Actions -
1.Lending a book-

The structure checks whether the subscriber ID exists in the subscriber tree, whether the ID corresponds to the name, can it
Loan another book and not currently lend 10 (maximum allowed) books
In addition, we will examine whether it can borrow the book it is interested in and whether it exists in the library at all).
The Books (.
If so, then a pointer to a book is inserted into the array at the subscription node, which points to the vertex of the requested book, the pointer
At the apex of the book will indicate the subscription node and the value of the books borrowed at the subscription node will increase by one.
Search and Insertion Subscriber Tree: Olg n
Is the number of subscribers in the library. n
Searching and finding the book, in the book tree: Olgm
Is the number of books in the library. m
Adding a book to an array at the subscription node and deleting and inserting a two-way link: Fixed actions.
Hence, O (lg max (m, n)).
