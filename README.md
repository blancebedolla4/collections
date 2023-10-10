*collections

Collection interface is the root interface for all collections in Java. To be considered a collection, certain methods must be implemented, including "add()", "size(), remove() and more
can be categorized into Lists and sets.

* set 
is a collection of unique values without an index.

*list
is an ordered group of values that are numerically indexed. Also an interface that implements methods  of the Collection interface and provides its own methods.

Problems with Arrays  
Arrays lack dynamic resizing capabilities, limiting flexibility

Lists offer dynamic resizing and can be easily converted to arrays using the toArray() method.

Adding elements to a List
example :
List<String> languages = new ArrayList<>();
languages.add ("Java");
System.out.Println(languages.size()):

Iterating through elements in a list 
use for loop

for (String language : languages)
System.out.println(language):

Working with index and value
System.out.println(languages.indexOf("Java"));
System.out.println(languages.get(0));


Removing Elements from a List
languages.remove("Java");
languages.remove(0);

subList()  method provides a view of the list. Modifying also affects original list

Map Interface
represent unordere collections of key-value pairs, indexed by keys.

Keys must be unique objects, while values can be repeated.

LinkedinHashMap preserves insertion order
TreeMap - sorts eleements by key

HashMap- no guaranteed order 
example:

Map<String, Integer> coursesByLanguage = new HashMap<>();
coursesByLanguage.put("HTML", 5);
coursesByLanguage.put("CSS", 3);
coursesByLanguage.put("JavaScript", 20);
System.out.println(coursesByLanguage.size()); // Outputs 3

Iterating through a map

for (Map.Entry<String, Integer> entry : coursesByLanguage.entrySet()) {
    System.out.format("%d %s courses%n", entry.getValue(), entry.getKey());
}










Commonly Used Collections

    List: Ordered collection, allows duplicates. (e.g., ArrayList, LinkedList)
    Set: Unordered collection, doesn't allow duplicates. (e.g., HashSet)
    SortedSet: Set with sorted elements. (e.g., TreeSet)
    Queue: Ordered collection for elements waiting to be processed. (e.g., PriorityQueue)
    Deque: Double-ended queue, allows insertion and removal from both ends. (e.g., ArrayDeque)
    Map: Key-value pairs, doesn't allow duplicate keys. (e.g., HashMap)
    SortedMap: Map with sorted keys. (e.g., TreeMap)


Choosing the Right Collection

    Elements are keyed:
        Yes? Order is important?
            If yes: SortedMap
            If no: Map
        Elements must be unique?
            If yes, is order important?
                If yes: SortedSet
                If no: Set
            If no: List


  List Operations and Features

Lists are ordered collections where each element has an index. Key features include:

    Add at Index: void add(int index, E element)
    Read by Index: E get(int index)
    Remove by Index: E remove(int index)
    Update by Index: E set(int index, E element)
    Lookup Indices by Value: int indexOf(Object o), int lastIndexOf(Object o)
    Sublists: Views over ranges of lists
    Sorting: Using comparators


    Set and SortedSet

    Set: Unordered collection, doesn't allow duplicates. (e.g., HashSet)
    SortedSet: Set with sorted elements. (e.g., TreeSet)

Queue and Deque

    Queue: Ordered collection for elements waiting to be processed. (e.g., PriorityQueue)
    Deque: Double-ended queue, allows insertion and removal from both ends. (e.g., ArrayDeque)

Map and SortedMap

    Map: Key-value pairs, doesn't allow duplicate keys. (e.g., HashMap)
    SortedMap: Map with sorted keys. (e.g., TreeMap)

Collection Behaviors

    Common Operations:
        size(), isEmpty(), add(), addAll(), remove(), removeAll(), retainAll(), contains(), containsAll(), clear()

  List-specific Features

    Static Factory Methods: Create unmodifiable list instances
    Overloads: Support for 0-10 arguments
    Varargs Constructor: For more than 10 arguments
    Unmodifiable Copies: Create unmodifiable lists from existing collections

Sublists and Modifications

    Sublists: Views over ranges of lists
    Modifying the View: Modifications reflect on the original list

Sorting and Comparators

    Sorting: Lists can be sorted using comparators for custom ordering


    Static Factory Methods

    Creates Unmodifiable Lists: Instances with various arguments and varargs constructor




