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

<h2>51. MaxUploadSizeExceededException</h2>
<p><strong>Fix:</strong> Increase <code>spring.servlet.multipart.max-file-size</code>.</p>

<h2>52. HttpMediaTypeNotSupportedException</h2>
<p><strong>Fix:</strong> Set correct Content-Type in request.</p>

<h2>53. HttpMediaTypeNotAcceptableException</h2>
<p><strong>Fix:</strong> Set Accept header correctly.</p>

<h2>54. MissingPathVariableException</h2>
<p><strong>Fix:</strong> Ensure URL path variable matches <code>@PathVariable</code> param.</p>

<h2>55. MethodArgumentTypeMismatchException</h2>
<p><strong>Fix:</strong> Use correct param type or add converter.</p>

<h2>56. BindException</h2>
<p><strong>Fix:</strong> Check DTO validation annotations.</p>

<h2>57. BeanInstantiationException</h2>
<p><strong>Fix:</strong> Ensure default constructor present or proper factory method.</p>

<h2>58. ClassNotFoundException</h2>
<p><strong>Fix:</strong> Check dependencies and imports.</p>

<h2>59. NoSuchMethodException</h2>
<p><strong>Fix:</strong> Validate method signature or refactor code.</p>

<h2>60. IllegalAccessException</h2>
<p><strong>Fix:</strong> Ensure field/method visibility or use reflection properly.</p>

<h2>61. InvocationTargetException</h2>
<p><strong>Fix:</strong> Check underlying exception in reflective call.</p>

<h2>62. NoSuchBeanDefinitionException</h2>
<p><strong>Fix:</strong> Ensure correct package scanning and bean annotation.</p>

<h2>63. TypeMismatchException</h2>
<p><strong>Fix:</strong> Convert property types correctly.</p>
<h2>64. PropertyReferenceException</h2>
<p><strong>Fix:</strong> Check Spring Data JPA query method names.</p>

<h2>65. QueryTimeoutException</h2>
<p><strong>Fix:</strong> Increase timeout or optimize query.</p>

<h2>66. IncorrectResultSizeDataAccessException</h2>
<p><strong>Fix:</strong> Ensure query returns expected number of rows.</p>

<h2>67. EmptyResultDataAccessException</h2>
<p><strong>Fix:</strong> Handle empty result in repository/service.</p>

<h2>68. OptimisticLockingFailureException</h2>
<p><strong>Fix:</strong> Check versioning in entity and handle concurrency.</p>

<h2>69. StaleStateException</h2>
<p><strong>Fix:</strong> Refresh entity before update or use merge.</p>

<h2>70. BeanDefinitionStoreException</h2>
<p><strong>Fix:</strong> Check config classes and context setup.</p>
<h2>71. UnsatisfiedDependencyException</h2>
<p><strong>Fix:</strong> Verify bean injection and circular dependency.</p>

<h2>72. ValidationException</h2>
<p><strong>Fix:</strong> Check DTO annotations and custom validators.</p>

<h2>73. ConstraintViolationException</h2>
<p><strong>Fix:</strong> Ensure entity constraints and DB schema match.</p>

<h2>74. DataIntegrityViolationException</h2>
<p><strong>Fix:</strong> Check unique constraints and entity mapping.</p>

<h2>75. HttpClientErrorException</h2>
<p><strong>Fix:</strong> Verify REST call URL, method, and payload.</p>

<h2>76. HttpServerErrorException</h2>
<p><strong>Fix:</strong> Check server side logs and exception stacktrace.</p>

<h2>77. ResourceAccessException</h2>
<p><strong>Fix:</strong> Ensure endpoint reachable and firewall allows connection.</p>

<h2>78. SocketTimeoutException</h2>
<p><strong>Fix:</strong> Increase timeout in RestTemplate or WebClient.</p>

<h2>79. ConnectException</h2>
<p><strong>Fix:</strong> Check server is running and port accessible.</p>

<h2>80. JsonMappingException</h2>
<p><strong>Fix:</strong> Check DTO structure and JSON format.</p>

<h2>81. MissingServletRequestParameterException</h2>
<p><strong>Fix:</strong> Add required request param or mark optional.</p>

<h2>82. HttpMessageNotReadableException</h2>
<p><strong>Fix:</strong> Verify request body JSON.</p>

<h2>83. HttpMessageNotWritableException</h2>
<p><strong>Fix:</strong> Verify response DTO mapping and serializers.</p>

<h2>84. MethodArgumentNotValidException</h2>
<p><strong>Fix:</strong> Validate request body and handle binding result.</p>

<h2>85. NoHandlerFoundException</h2>
<p><strong>Fix:</strong> Add <code>@ControllerAdvice</code> or correct endpoint mapping.</p>

<h2>86. AccessDeniedException</h2>
<p><strong>Fix:</strong> Configure Spring Security properly.</p>

<h2>87. AuthenticationException</h2>
<p><strong>Fix:</strong> Check auth manager and credentials.</p>

<h2>88. BadCredentialsException</h2>
<p><strong>Fix:</strong> Verify user password and encoding.</p>


