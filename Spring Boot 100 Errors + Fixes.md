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
