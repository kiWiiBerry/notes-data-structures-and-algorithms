# HashSet

#### Convert Array to Set

```text
// import java.util.Arrays;
// import java.util.stream.Collectors;
// import java.util.Set;

int[] nums = new int[]{1, 2, 3};
Set<Integer> set = Arrays.stream(nums).boxed().collect(Collectors.toSet());

// Print out the elements in set
System.out.println(set.toString());
```

#### Convert Set to Array

```text
int[] numsNew = set.stream().mapToInt(Number::intValue).toArray();

// Print out the elements in array
System.out.println(Arrays.toString(numsNew));
```

