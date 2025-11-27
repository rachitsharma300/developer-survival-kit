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

<h2>3. Convert CheatCodes</h2>
<ul>
  <li><code>String str = String.valueOf(123);</code></li>
  <li><code>int n = Integer.parseInt("10");</code></li>
  <li><code>double d = Double.parseDouble("10.5");</code></li>
  <li><code>String arrStr = Arrays.toString(new int[]{1,2,3});</code></li>
  <li><code>List&lt;String&gt; l = Arrays.asList(str.split(","));</code></li>
  <li><code>int[] arr = list.stream().mapToInt(Integer::parseInt).toArray();</code></li>
  <li><code>LocalDate date = LocalDate.parse("2024-01-11");</code></li>
  <li><code>Date now = new Date();</code></li>
  <li><code>String json = new ObjectMapper().writeValueAsString(obj);</code></li>
  <li><code>MyClass obj = new ObjectMapper().readValue(json, MyClass.class);</code></li>
</ul>

<h2>4. DSA Quick Templates</h2>
<ul>
  <li><code>// Binary Search
int bs(int[] arr, int target) {
 int l=0, r=arr.length-1;
 while(l&lt;=r){
  int mid = l+(r-l)/2;
  if(arr[mid]==target) return mid;
  else if(arr[mid]&lt;target) l=mid+1;
  else r=mid-1;
 }
 return -1;
}</code></li>

  <li><code>// Two Pointer
while(l &lt; r){
 int sum = arr[l] + arr[r];
 if(sum == target) break;
 else if(sum &lt; target) l++;
 else r--;
}</code></li>

  <li><code>// Sliding Window
int sum=0, l=0;
for(int r=0; r&lt;n; r++){
 sum+=arr[r];
 while(sum &gt; k){
  sum-=arr[l++];
 }
}</code></li>

  <li><code>// Frequency Map
Map&lt;Integer,Integer&gt; freq = new HashMap<>();
for(int x: arr) freq.put(x, freq.getOrDefault(x,0)+1);
</code></li>

  <li><code>// Reverse String
new StringBuilder(str).reverse().toString();</code></li>
</ul>

<h2>5. String CheatCodes</h2>
<ul>
  <li><code>str.toLowerCase()</code></li>
  <li><code>str.toUpperCase()</code></li>
  <li><code>str.trim()</code></li>
  <li><code>str.replace("a","b")</code></li>
  <li><code>str.contains("abc")</code></li>
  <li><code>str.startsWith("A")</code></li>
  <li><code>str.endsWith("Z")</code></li>
  <li><code>str.substring(1,4)</code></li>
  <li><code>str.matches("[0-9]+")</code></li>
  <li><code>String.join("-", list)</code></li>
</ul>

<h2>6. OOP CheatCodes</h2>
<ul>
  <li><code>class A { private int x; }</code></li>
  <li><code>class B extends A {}</code></li>
  <li><code>interface Test { void run(); }</code></li>
  <li><code>abstract class Animal { abstract void sound(); }</code></li>
  <li><code>@Override public String toString(){ return "Hi"; }</code></li>
  <li><code>public static final String NAME = "Rachit";</code></li>
  <li><code>private static A instance = new A();</code></li>
  <li><code>Singleton.getInstance();</code></li>
  <li><code>Optional.ofNullable(obj)</code></li>
  <li><code>record User(String name, int age) {}</code></li>
</ul>

<h2>7. File Handling</h2>
<ul>
  <li><code>Files.readString(Path.of("a.txt"));</code></li>
  <li><code>Files.writeString(Path.of("a.txt"), "Hello");</code></li>
  <li><code>List&lt;String&gt; lines = Files.readAllLines(Path.of("file.txt"));</code></li>
  <li><code>Files.copy(Path.of("a.txt"), Path.of("b.txt"));</code></li>
  <li><code>Files.delete(Path.of("a.txt"));</code></li>
  <li><code>Files.exists(Path.of("a.txt"));</code></li>
  <li><code>new File("folder").mkdir();</code></li>
  <li><code>new File("folder").listFiles();</code></li>
  <li><code>BufferedReader br = new BufferedReader(new FileReader("a.txt"));</code></li>
  <li><code>BufferedWriter bw = new BufferedWriter(new FileWriter("b.txt"));</code></li>
</ul>

<h2>8. Exception Handling</h2>
<ul>
  <li><code>try{} catch(Exception e){ e.printStackTrace(); }</code></li>
  <li><code>throw new RuntimeException("Error!");</code></li>
  <li><code>Objects.requireNonNull(obj);</code></li>
  <li><code>assert x &gt; 0;</code></li>
  <li><code>Optional.ofNullable(obj).orElse("NA");</code></li>
</ul>

<h2>9. Multi-threading</h2>
<ul>
  <li><code>Thread t = new Thread(() -&gt; System.out.println("Hi")); t.start();</code></li>
  <li><code>Runnable r = () -&gt; System.out.println("Run");</code></li>
  <li><code>ExecutorService ex = Executors.newFixedThreadPool(5);</code></li>
  <li><code>ex.submit(() -&gt; System.out.println("Task"));</code></li>
  <li><code>ex.shutdown();</code></li>
  <li><code>CompletableFuture.supplyAsync(() -&gt; "Hello").thenAccept(System.out::println);</code></li>
  <li><code>Thread.sleep(1000);</code></li>
  <li><code>ReentrantLock lock = new ReentrantLock();</code></li>
  <li><code>synchronized(this){ }</code></li>
  <li><code>AtomicInteger ai = new AtomicInteger(0); ai.incrementAndGet();</code></li>
</ul>
