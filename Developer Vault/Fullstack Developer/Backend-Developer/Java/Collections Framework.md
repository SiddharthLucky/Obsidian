#Java-Concepts

Understanding of interfaces like List, Set, Map, and their implementations (ArrayList, HashSet, HashMap, etc.).

1. **Set**: Set is an interface in the Java Collections Framework and extends the Collection interface. It represents a collection of objects where every object is unique.
2. **Map**: Map is an object that maps keys to values. A map cannot contain duplicate keys; each key can map to at most one value.
1. **HashSet**: HashSet is a class which implements Set Interface. It does not maintain the insertion order and allows the insertion of null elements.
2. **LinkedHashSet**: LinkedHashSet is a class that extends HashSet and maintains the insertion order.
3. **TreeSet**: TreeSet is a NavigableSet implementation where elements are sorted in ascending order.
4. **HashMap**: HashMap is a class that implements Map interface. It does not maintain any order of its keys and allows one null key and multiple null values.
5. **LinkedHashMap**: LinkedHashMap is a class that extends HashMap and maintains insertion order of keys.
6. **TreeMap**: TreeMap is a class that implements NavigableMap interface. It maintains ascending order of its keys.
7. **HashMap vs HashSet**: The main difference is that Map interface is implemented by different classes like HashMap, TreeMap, LinkedHashMap whereas Set interface is implemented by HashSet, LinkedHashSet, TreeSet.
8. **Complexity**: For HashSet and HashMap, the best-case (no collisions) time complexity for add, remove, and search is O(1). For TreeSet and TreeMap, these operations run in O(log n) time.