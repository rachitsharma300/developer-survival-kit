<h1>Java CheatCodes - 100 Killer Snippets</h1>

<h2>1. Collections (List / Map / Set)</h2>
<ul>
  <li><code>List&lt;String&gt; list = Arrays.asList("A","B","C");</code></li>
  <li><code>List&lt;Integer&gt; nums = Arrays.stream(new int[]{1,2,3}).boxed().toList();</code></li>
  <li><code>List&lt;String&gt; copy = new ArrayList<>(list);</code></li>
  <li><code>Collections.sort(list);</code></li>
  <li><code>Collections.reverse(list);</code></li>
  <li><code>Set&lt;String&gt; set = new HashSet<>(list);</code></li>
  <li><code>Map&lt;String,Integer&gt; map = Map.of("a",1,"b",2);</code></li>
  <li><code>map.forEach((k,v) -&gt; System.out.println(k + ":" + v));</code></li>
  <li><code>Map&lt;String, Long&gt; freq = list.stream().collect(Collectors.groupingBy(e-&gt;e, Collectors.counting()));</code></li>
  <li><code>list.removeIf(x -&gt; x.startsWith("A"));</code></li>
</ul>

<h2>2. Streams CheatCodes</h2>
<ul>
  <li><code>list.stream().filter(x -&gt; x.contains("a")).toList();</code></li>
  <li><code>list.stream().map(String::toUpperCase).toList();</code></li>
  <li><code>list.stream().sorted().toList();</code></li>
  <li><code>list.stream().distinct().toList();</code></li>
  <li><code>list.stream().limit(5).toList();</code></li>
  <li><code>int sum = nums.stream().mapToInt(i -&gt; i).sum();</code></li>
  <li><code>int max = nums.stream().max(Integer::compare).orElse(0);</code></li>
  <li><code>int min = nums.stream().min(Integer::compare).orElse(0);</code></li>
  <li><code>boolean any = list.stream().anyMatch(x -&gt; x.equals("A"));</code></li>
  <li><code>String join = list.stream().collect(Collectors.joining(", "));</code></li>
</ul>
