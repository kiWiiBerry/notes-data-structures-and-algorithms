# String, StringBuilder

### String

Convert a string of a number to corresponding integer: `Integer.valueOf()`.

Convert a char array to string: `String.valueOf(aCharArray)`.

```text
charAt(int index)
compareTo(String anotherString)
compareToIgnoreCase(String str)
contains(CharSequence s)
copyValueOf(char[] data, int offset, int count)
endsWith(String suffix)
equals(Object anObject)
equalsIgnoreCase(String anotherString)
getBytes()
```

```text
indexOf(String ch)
indexOf(String ch, int fromIndex)
lastIndexOf(String str)
lastIndexOf(String str, int fromIndex)
isEmpty()
length()
```

```text
replace(char oldChar, char newChar)
replaceAll(String regex, String replacement)
replaceFirst(String regex, String replacement)
```

```text
split(String regex, int limit)
trim()
startsWith(String prefix)
startsWith(String prefix, int offset)
```

```text
substring(int beginIndex, int endIndex)
valueOf(Object obj)
```

```text
toCharArray()
toLowerCase()
toUpperCase()
```



### StringBuilder

Except for similar methods as String class, below are other useful methods of StringBuilder.

```text
append(String str)
capacity()
deleteCharAt(int index)
insert(int dstOffset, CharSequence s)
insert(int dstOffset, CharSequence s, int start, int end)
insert(int index, char[] str, int offset, int len)
reverse()
replace(int start, int end, String str)
subSequence(int start, int end)
substring(int start, int end)
```

