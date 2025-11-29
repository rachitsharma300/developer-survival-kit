<h1>Spring Boot 100 Common Errors & Fixes</h1>

<h2>1. Circular Dependency</h2>
<p><strong>Error:</strong> BeanCurrentlyInCreationException</p>
<p><strong>Fix:</strong> Use <code>@Lazy</code> on one of the dependent beans or restructure your dependencies.</p>

<h2>2. 403 Forbidden</h2>
<p><strong>Error:</strong> Access denied for endpoint</p>
<p><strong>Fix:</strong> Check Spring Security configuration. Ensure roles and authorities are properly mapped.</p>

<h2>3. Bean Creation Failed</h2>
<p><strong>Error:</strong> UnsatisfiedDependencyException / NoSuchBeanDefinitionException</p>
<p><strong>Fix:</strong> Make sure your <code>@Component/@Service/@Repository</code> beans are properly annotated and scanned.</p>
<h2>4. CORS Error</h2>
<p><strong>Error:</strong> Cross-Origin request blocked</p>
<p><strong>Fix:</strong> Add <code>@CrossOrigin</code> on controller or configure global CORS in WebMvcConfigurer.</p>

<h2>5. HikariPool Connection Timeout</h2>
<p><strong>Error:</strong> Failed to obtain connection from Hikari pool</p>
<p><strong>Fix:</strong> Check DB URL, credentials, max pool size, or DB server availability.</p>

<h2>6. MongoDB Connection Timeout</h2>
<p><strong>Error:</strong> Could not connect to MongoDB</p>
<p><strong>Fix:</strong> Verify MongoDB URI, network, and firewall. Ensure MongoDB service is running.</p>

<h2>7. ApplicationContext Failed to Start</h2>
<p><strong>Error:</strong> ContextLoadException</p>
<p><strong>Fix:</strong> Check bean configuration, missing properties, or invalid @Value injection.</p>

<h2>8. Port Already in Use</h2>
<p><strong>Error:</strong> Embedded Tomcat failed to start</p>
<p><strong>Fix:</strong> Change server.port in <code>application.properties</code> or kill existing process using port.</p>

<h2>9. Invalid Property Configuration</h2>
<p><strong>Error:</strong> BindException / ConfigurationProperties error</p>
<p><strong>Fix:</strong> Check property names, types, and proper prefix in <code>@ConfigurationProperties</code>.</p>

<h2>10. Failed to Load ApplicationContext</h2>
<p><strong>Error:</strong> Test context fails</p>
<p><strong>Fix:</strong> Ensure test classes have proper <code>@SpringBootTest</code> annotation and mocks.</p>

<h2>11. NoSuchMethodError / ClassNotFoundException</h2>
<p><strong>Fix:</strong> Check dependency versions in <code>pom.xml</code> or <code>build.gradle</code>. Resolve conflicts.</p>

<h2>12. Invalid JWT Token</h2>
<p><strong>Error:</strong> SignatureException / MalformedJwtException</p>
<p><strong>Fix:</strong> Verify secret key, algorithm, and token expiration.</p>

<h2>13. MethodArgumentNotValidException</h2>
<p><strong>Error:</strong> Validation failed for @RequestBody</p>
<p><strong>Fix:</strong> Use proper <code>@Valid</code> annotations and binding results checks.</p>
<h2>14. DataIntegrityViolationException</h2>
<p><strong>Error:</strong> Duplicate key or constraint violation</p>
<p><strong>Fix:</strong> Check entity constraints and DB uniqueness rules.</p>

<h2>15. LazyInitializationException</h2>
<p><strong>Error:</strong> Could not initialize proxy - no Session</p>
<p><strong>Fix:</strong> Use <code>@Transactional</code> or fetch joins to initialize lazy associations.</p>

<h2>16. HTTP 500 Internal Server Error</h2>
<p><strong>Fix:</strong> Check controller, service, and repository layers for null pointer or unhandled exceptions.</p>

<h2>17. File Upload Error</h2>
<p><strong>Error:</strong> MultipartException / MaxUploadSizeExceededException</p>
<p><strong>Fix:</strong> Configure <code>spring.servlet.multipart.max-file-size</code> and <code>max-request-size</code>.</p>

<h2>18. JSON Parse Error</h2>
<p><strong>Error:</strong> HttpMessageNotReadableException</p>
<p><strong>Fix:</strong> Check JSON format and mapping DTOs.</p>

<h2>19. SQL Syntax Error</h2>
<p><strong>Fix:</strong> Validate queries in repository or use JPA methods.</p>

<h2>20. Transaction Rollback Exception</h2>
<p><strong>Fix:</strong> Ensure proper <code>@Transactional</code> usage and exception handling.</p>

<h2>21. Bean Definition Overriding</h2>
<p><strong>Error:</strong> BeanDefinitionOverrideException</p>
<p><strong>Fix:</strong> Enable overriding or rename beans.</p>

<h2>22. Missing Servlet Mapping</h2>
<p><strong>Fix:</strong> Add correct <code>@RequestMapping</code> or <code>@GetMapping/@PostMapping</code>.</p>

<h2>23. Template Engine Error (Thymeleaf/Freemarker)</h2>
<p><strong>Fix:</strong> Check template path, variable names, and configuration.</p>

<h2>24. SSL/TLS Handshake Exception</h2>
<p><strong>Fix:</strong> Import correct certificates or trust store for HTTPS connection.</p>

<h2>25. Spring Security UsernameNotFoundException</h2>
<p><strong>Fix:</strong> Ensure UserDetailsService implementation returns valid user object.</p>
<h2>26. HTTP 404 Not Found</h2>
<p><strong>Fix:</strong> Verify controller endpoint mapping and URL patterns.</p>

<h2>27. MethodNotAllowed 405</h2>
<p><strong>Fix:</strong> Ensure HTTP method matches the controller mapping (GET/POST/PUT/DELETE).</p>

<h2>28. Multipart File Encoding Error</h2>
<p><strong>Fix:</strong> Set <code>spring.http.multipart.enabled=true</code> and proper encoding.</p>

<h2>29. Hibernate Validator Error</h2>
<p><strong>Fix:</strong> Use proper annotations (<code>@NotNull, @Size</code>) and validate request body.</p>

<h2>30. BeanNotOfRequiredTypeException</h2>
<p><strong>Fix:</strong> Ensure correct generic types and bean injection types.</p>
<h2>31. PropertySourceNotFoundException</h2>
<p><strong>Fix:</strong> Check property file location and <code>@PropertySource</code> usage.</p>

<h2>32. MissingServletRequestParameterException</h2>
<p><strong>Fix:</strong> Ensure request params are present or mark as optional with <code>required=false</code>.</p>

<h2>33. TypeMismatchException</h2>
<p><strong>Fix:</strong> Convert parameter type correctly or use <code>@RequestParam(required=false)</code>.</p>

<h2>34. ConversionFailedException</h2>
<p><strong>Fix:</strong> Add proper converters or use compatible data types.</p>

<h2>35. InvalidFormatException</h2>
<p><strong>Fix:</strong> Map JSON fields correctly and use proper date format.</p>

<h2>36. HttpMessageConversionException</h2>
<p><strong>Fix:</strong> Check request and response DTO mapping.</p>

<h2>37. MissingServletRequestPartException</h2>
<p><strong>Fix:</strong> Ensure multipart form-data has correct parts.</p>

<h2>38. IllegalStateException - Session Closed</h2>
<p><strong>Fix:</strong> Avoid accessing lazy-loaded entities outside transaction.</p>

<h2>39. ClassCastException</h2>
<p><strong>Fix:</strong> Ensure correct type casting and generics.</p>

<h2>40. IllegalArgumentException</h2>
<p><strong>Fix:</strong> Validate input params and DTOs.</p>

<h2>41. NoUniqueBeanDefinitionException</h2>
<p><strong>Fix:</strong> Use <code>@Primary</code> or rename beans.</p>

<h2>42. UnsatisfiedDependencyException</h2>
<p><strong>Fix:</strong> Check constructor or field injection for missing beans.</p>

<h2>43. Circular Reference in Configuration</h2>
<p><strong>Fix:</strong> Restructure @Configuration classes or mark bean lazy.</p>

<h2>44. BeanCurrentlyInCreationException</h2>
<p><strong>Fix:</strong> Use <code>@Lazy</code> or restructure dependent beans.</p>

<h2>45. TransactionTimedOutException</h2>
<p><strong>Fix:</strong> Increase transaction timeout or optimize DB operations.</p>

<h2>46. DataAccessResourceFailureException</h2>
<p><strong>Fix:</strong> Ensure DB connectivity and credentials.</p>

<h2>47. CannotCreateTransactionException</h2>
<p><strong>Fix:</strong> Verify DB connection pool and isolation level.</p>

<h2>48. SQLGrammarException</h2>
<p><strong>Fix:</strong> Validate SQL queries or use JPA methods.</p>

<h2>49. LazyInitializationException</h2>
<p><strong>Fix:</strong> Use <code>@Transactional</code> or eager fetch joins.</p>

<h2>50. JDBC Connection Exception</h2>
<p><strong>Fix:</strong> Check DB URL, credentials, driver dependency.</p>



