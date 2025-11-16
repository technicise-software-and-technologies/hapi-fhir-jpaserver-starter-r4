mvn clean install
[INFO] Scanning for projects...
[WARNING] 
[WARNING] Some problems were encountered while building the effective model for ca.uhn.hapi.fhir:hapi-fhir-jpaserver-starter:war:8.4.0-4
[WARNING] 'version' contains an expression but should be a constant. @ ca.uhn.hapi.fhir:hapi-fhir-jpaserver-starter:${project.parent.version}-${hapi.fhir.jpa.server.starter.revision}, /media/chandra/b664505e-129c-4c0d-a87b-9efb6469eca2/home/chandra/code/hapi-fhir-jpaserver-starter/pom.xml, line 27, column 14
[WARNING] 
[WARNING] It is highly recommended to fix these problems because they threaten the stability of your build.
[WARNING] 
[WARNING] For this reason, future Maven versions might no longer support building such malformed projects.
[WARNING] 
[WARNING] The project ca.uhn.hapi.fhir:hapi-fhir-jpaserver-starter:war:8.4.0-4 uses prerequisites which is only intended for maven-plugin projects but not for non maven-plugin projects. For such purposes you should use the maven-enforcer-plugin. See https://maven.apache.org/enforcer/enforcer-rules/requireMavenVersion.html
[INFO] 
[INFO] ------------< ca.uhn.hapi.fhir:hapi-fhir-jpaserver-starter >------------
[INFO] Building HAPI FHIR JPA Server - Starter Project 8.4.0-4
[INFO]   from pom.xml
[INFO] --------------------------------[ war ]---------------------------------
[INFO] 
[INFO] --- clean:3.4.0:clean (default-clean) @ hapi-fhir-jpaserver-starter ---
[INFO] 
[INFO] --- enforcer:3.5.0:enforce (enforce-maven) @ hapi-fhir-jpaserver-starter ---
[INFO] Rule 0: org.apache.maven.enforcer.rules.version.RequireMavenVersion passed
[INFO] Rule 1: org.apache.maven.enforcer.rules.version.RequireJavaVersion passed
[INFO] 
[INFO] --- resources:3.3.0:resources (default-resources) @ hapi-fhir-jpaserver-starter ---
[INFO] Copying 4 resources
[INFO] 
[INFO] --- compiler:3.13.0:compile (default-compile) @ hapi-fhir-jpaserver-starter ---
[INFO] Recompiling the module because of changed source code.
[INFO] Compiling 70 source files with javac [forked debug release 17] to target/classes
[WARNING] Unable to autodetect 'javac' path, using 'javac' from the environment.
[INFO] 
[INFO] --- resources:3.3.0:testResources (default-testResources) @ hapi-fhir-jpaserver-starter ---
[INFO] Copying 23 resources
[INFO] 
[INFO] --- compiler:3.13.0:testCompile (default-testCompile) @ hapi-fhir-jpaserver-starter ---
[INFO] Recompiling the module because of changed dependency.
[INFO] Compiling 25 source files with javac [forked debug release 17] to target/test-classes
[WARNING] Unable to autodetect 'javac' path, using 'javac' from the environment.
[INFO] 
[INFO] --- surefire:3.4.0:test (default-test) @ hapi-fhir-jpaserver-starter ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running ca.uhn.fhir.jpa.starter.CustomInterceptorTest
[INFO] Running ca.uhn.fhir.jpa.starter.MdmTest
[INFO] Running ca.uhn.fhir.jpa.starter.CustomOperationTest
[INFO] Running ca.uhn.fhir.jpa.starter.CustomBeanTest
[ERROR] Tests run: 1, Failures: 0, Errors: 1, Skipped: 0, Time elapsed: 31.02 s <<< FAILURE! -- in ca.uhn.fhir.jpa.starter.CustomInterceptorTest
[ERROR] ca.uhn.fhir.jpa.starter.CustomInterceptorTest.testAuditInterceptors -- Time elapsed: 0.019 s <<< ERROR!
java.lang.IllegalStateException: Failed to load ApplicationContext for [WebMergedContextConfiguration@aae69d3 testClass = ca.uhn.fhir.jpa.starter.CustomInterceptorTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "hapi.fhir.custom-interceptor-classes=some.custom.pkg1.CustomInterceptorBean,some.custom.pkg1.CustomInterceptorPojo", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.cr_enabled=false", "hapi.fhir.fhir_version=r4", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:180)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
Caused by: org.springframework.context.ApplicationContextException: Unable to start web server
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:170)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:619)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
        at org.springframework.boot.test.context.SpringBootContextLoader.lambda$loadContext$3(SpringBootContextLoader.java:145)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:58)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:46)
        at org.springframework.boot.SpringApplication.withHook(SpringApplication.java:1464)
        at org.springframework.boot.test.context.SpringBootContextLoader$ContextLoaderHook.run(SpringBootContextLoader.java:564)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:145)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:116)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContextInternal(DefaultCacheAwareContextLoaderDelegate.java:225)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:152)
        ... 17 more
Caused by: org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:147)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.<init>(TomcatWebServer.java:107)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getTomcatWebServer(TomcatServletWebServerFactory.java:520)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getWebServer(TomcatServletWebServerFactory.java:222)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.createWebServer(ServletWebServerApplicationContext.java:193)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:167)
        ... 31 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'hapiServletRegistration' defined in ca.uhn.fhir.jpa.starter.Application: Unsatisfied dependency expressed through method 'hapiServletRegistration' parameter 0: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:205)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:211)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:202)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.addServletContextInitializerBeans(ServletContextInitializerBeans.java:97)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.<init>(ServletContextInitializerBeans.java:86)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.getServletContextInitializerBeans(ServletWebServerApplicationContext.java:271)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.selfInitialize(ServletWebServerApplicationContext.java:245)
        at org.springframework.boot.web.embedded.tomcat.TomcatStarter.onStartup(TomcatStarter.java:52)
        at org.apache.catalina.core.StandardContext.startInternal(StandardContext.java:4464)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardHost.startInternal(StandardHost.java:772)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardEngine.startInternal(StandardEngine.java:203)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardService.startInternal(StandardService.java:412)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardServer.startInternal(StandardServer.java:870)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.startup.Tomcat.start(Tomcat.java:438)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:128)
        ... 36 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 76 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:388)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1439)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:599)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 90 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'entityManagerFactory' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1806)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:600)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:225)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1328)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1289)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1257)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findDefaultEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:593)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:557)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.resolveEntityManager(PersistenceAnnotationBeanPostProcessor.java:724)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.getResourceToInject(PersistenceAnnotationBeanPostProcessor.java:697)
        at org.springframework.beans.factory.annotation.InjectionMetadata$InjectedElement.inject(InjectionMetadata.java:270)
        at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:145)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:385)
        ... 102 more
Caused by: jakarta.persistence.PersistenceException: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:421)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.afterPropertiesSet(AbstractEntityManagerFactoryBean.java:396)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.afterPropertiesSet(LocalContainerEntityManagerFactoryBean.java:366)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1853)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1802)
        ... 118 more
Caused by: java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at com.zaxxer.hikari.util.DriverDataSource.<init>(DriverDataSource.java:110)
        at com.zaxxer.hikari.pool.PoolBase.initializeDataSource(PoolBase.java:326)
        at com.zaxxer.hikari.pool.PoolBase.<init>(PoolBase.java:112)
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:93)
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112)
        at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:126)
        at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:467)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:46)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:39)
        at org.hibernate.tool.schema.internal.exec.ImprovedExtractionContextImpl.getJdbcConnection(ImprovedExtractionContextImpl.java:63)
        at org.hibernate.tool.schema.extract.spi.ExtractionContext.getQueryResults(ExtractionContext.java:43)
        at org.hibernate.tool.schema.extract.internal.SequenceInformationExtractorLegacyImpl.extractMetadata(SequenceInformationExtractorLegacyImpl.java:39)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.initializeSequences(DatabaseInformationImpl.java:66)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.<init>(DatabaseInformationImpl.java:60)
        at org.hibernate.tool.schema.internal.Helper.buildDatabaseInformation(Helper.java:185)
        at org.hibernate.tool.schema.internal.AbstractSchemaMigrator.doMigration(AbstractSchemaMigrator.java:93)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.performDatabaseAction(SchemaManagementToolCoordinator.java:280)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.lambda$process$5(SchemaManagementToolCoordinator.java:144)
        at java.base/java.util.HashMap.forEach(HashMap.java:1421)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.process(SchemaManagementToolCoordinator.java:141)
        at org.hibernate.boot.internal.SessionFactoryObserverForSchemaExport.sessionFactoryCreated(SessionFactoryObserverForSchemaExport.java:37)
        at org.hibernate.internal.SessionFactoryObserverChain.sessionFactoryCreated(SessionFactoryObserverChain.java:35)
        at org.hibernate.internal.SessionFactoryImpl.<init>(SessionFactoryImpl.java:324)
        at org.hibernate.boot.internal.SessionFactoryBuilderImpl.build(SessionFactoryBuilderImpl.java:463)
        at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:1506)
        at org.hibernate.jpa.HibernatePersistenceProvider.createContainerEntityManagerFactory(HibernatePersistenceProvider.java:142)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.createNativeEntityManagerFactory(LocalContainerEntityManagerFactoryBean.java:390)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:409)
        ... 122 more

[ERROR] Tests run: 1, Failures: 0, Errors: 1, Skipped: 0, Time elapsed: 30.99 s <<< FAILURE! -- in ca.uhn.fhir.jpa.starter.CustomBeanTest
[ERROR] ca.uhn.fhir.jpa.starter.CustomBeanTest.testCustomBeanExists -- Time elapsed: 0.018 s <<< ERROR!
java.lang.IllegalStateException: Failed to load ApplicationContext for [WebMergedContextConfiguration@66968a15 testClass = ca.uhn.fhir.jpa.starter.CustomBeanTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1,some.custom.pkg2", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.enable_repository_validating_interceptor=true", "hapi.fhir.fhir_version=r4", "hapi.fhir.mdm_enabled=false", "hapi.fhir.cr_enabled=false", "hapi.fhir.subscription.websocket_enabled=false", "spring.main.allow-bean-definition-overriding=true", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@6b7906b3, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@52d239ba, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@3f390d63, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@4e858e0a, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@42f33b5d, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@11981797, org.springframework.boot.test.context.SpringBootTestAnnotation@bbb9a93c], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:180)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
Caused by: org.springframework.context.ApplicationContextException: Unable to start web server
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:170)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:619)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
        at org.springframework.boot.test.context.SpringBootContextLoader.lambda$loadContext$3(SpringBootContextLoader.java:145)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:58)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:46)
        at org.springframework.boot.SpringApplication.withHook(SpringApplication.java:1464)
        at org.springframework.boot.test.context.SpringBootContextLoader$ContextLoaderHook.run(SpringBootContextLoader.java:564)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:145)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:116)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContextInternal(DefaultCacheAwareContextLoaderDelegate.java:225)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:152)
        ... 17 more
Caused by: org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:147)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.<init>(TomcatWebServer.java:107)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getTomcatWebServer(TomcatServletWebServerFactory.java:520)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getWebServer(TomcatServletWebServerFactory.java:222)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.createWebServer(ServletWebServerApplicationContext.java:193)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:167)
        ... 31 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'hapiServletRegistration' defined in ca.uhn.fhir.jpa.starter.Application: Unsatisfied dependency expressed through method 'hapiServletRegistration' parameter 0: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:205)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:211)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:202)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.addServletContextInitializerBeans(ServletContextInitializerBeans.java:97)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.<init>(ServletContextInitializerBeans.java:86)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.getServletContextInitializerBeans(ServletWebServerApplicationContext.java:271)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.selfInitialize(ServletWebServerApplicationContext.java:245)
        at org.springframework.boot.web.embedded.tomcat.TomcatStarter.onStartup(TomcatStarter.java:52)
        at org.apache.catalina.core.StandardContext.startInternal(StandardContext.java:4464)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardHost.startInternal(StandardHost.java:772)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardEngine.startInternal(StandardEngine.java:203)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardService.startInternal(StandardService.java:412)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardServer.startInternal(StandardServer.java:870)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.startup.Tomcat.start(Tomcat.java:438)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:128)
        ... 36 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 76 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:388)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1439)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:599)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 90 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'entityManagerFactory' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1806)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:600)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:225)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1328)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1289)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1257)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findDefaultEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:593)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:557)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.resolveEntityManager(PersistenceAnnotationBeanPostProcessor.java:724)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.getResourceToInject(PersistenceAnnotationBeanPostProcessor.java:697)
        at org.springframework.beans.factory.annotation.InjectionMetadata$InjectedElement.inject(InjectionMetadata.java:270)
        at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:145)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:385)
        ... 102 more
Caused by: jakarta.persistence.PersistenceException: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:421)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.afterPropertiesSet(AbstractEntityManagerFactoryBean.java:396)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.afterPropertiesSet(LocalContainerEntityManagerFactoryBean.java:366)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1853)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1802)
        ... 118 more
Caused by: java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at com.zaxxer.hikari.util.DriverDataSource.<init>(DriverDataSource.java:110)
        at com.zaxxer.hikari.pool.PoolBase.initializeDataSource(PoolBase.java:326)
        at com.zaxxer.hikari.pool.PoolBase.<init>(PoolBase.java:112)
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:93)
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112)
        at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:126)
        at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:467)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:46)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:39)
        at org.hibernate.tool.schema.internal.exec.ImprovedExtractionContextImpl.getJdbcConnection(ImprovedExtractionContextImpl.java:63)
        at org.hibernate.tool.schema.extract.spi.ExtractionContext.getQueryResults(ExtractionContext.java:43)
        at org.hibernate.tool.schema.extract.internal.SequenceInformationExtractorLegacyImpl.extractMetadata(SequenceInformationExtractorLegacyImpl.java:39)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.initializeSequences(DatabaseInformationImpl.java:66)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.<init>(DatabaseInformationImpl.java:60)
        at org.hibernate.tool.schema.internal.Helper.buildDatabaseInformation(Helper.java:185)
        at org.hibernate.tool.schema.internal.AbstractSchemaMigrator.doMigration(AbstractSchemaMigrator.java:93)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.performDatabaseAction(SchemaManagementToolCoordinator.java:280)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.lambda$process$5(SchemaManagementToolCoordinator.java:144)
        at java.base/java.util.HashMap.forEach(HashMap.java:1421)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.process(SchemaManagementToolCoordinator.java:141)
        at org.hibernate.boot.internal.SessionFactoryObserverForSchemaExport.sessionFactoryCreated(SessionFactoryObserverForSchemaExport.java:37)
        at org.hibernate.internal.SessionFactoryObserverChain.sessionFactoryCreated(SessionFactoryObserverChain.java:35)
        at org.hibernate.internal.SessionFactoryImpl.<init>(SessionFactoryImpl.java:324)
        at org.hibernate.boot.internal.SessionFactoryBuilderImpl.build(SessionFactoryBuilderImpl.java:463)
        at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:1506)
        at org.hibernate.jpa.HibernatePersistenceProvider.createContainerEntityManagerFactory(HibernatePersistenceProvider.java:142)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.createNativeEntityManagerFactory(LocalContainerEntityManagerFactoryBean.java:390)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:409)
        ... 122 more

[ERROR] Tests run: 1, Failures: 0, Errors: 1, Skipped: 0, Time elapsed: 31.04 s <<< FAILURE! -- in ca.uhn.fhir.jpa.starter.CustomOperationTest
[ERROR] ca.uhn.fhir.jpa.starter.CustomOperationTest.testCustomOperations -- Time elapsed: 0.026 s <<< ERROR!
java.lang.IllegalStateException: Failed to load ApplicationContext for [WebMergedContextConfiguration@7a4154c testClass = ca.uhn.fhir.jpa.starter.CustomOperationTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1", "hapi.fhir.custom-provider-classes=some.custom.pkg1.CustomOperationBean,some.custom.pkg1.CustomOperationPojo", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.cr_enabled=false", "hapi.fhir.fhir_version=r4", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@64a8c844, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@68ad99fe, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@85e6769, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@7ce97ee5, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@1951b871, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@6b44435b, org.springframework.boot.test.context.SpringBootTestAnnotation@d307348b], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:180)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
Caused by: org.springframework.context.ApplicationContextException: Unable to start web server
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:170)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:619)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
        at org.springframework.boot.test.context.SpringBootContextLoader.lambda$loadContext$3(SpringBootContextLoader.java:145)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:58)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:46)
        at org.springframework.boot.SpringApplication.withHook(SpringApplication.java:1464)
        at org.springframework.boot.test.context.SpringBootContextLoader$ContextLoaderHook.run(SpringBootContextLoader.java:564)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:145)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:116)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContextInternal(DefaultCacheAwareContextLoaderDelegate.java:225)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:152)
        ... 17 more
Caused by: org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:147)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.<init>(TomcatWebServer.java:107)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getTomcatWebServer(TomcatServletWebServerFactory.java:520)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getWebServer(TomcatServletWebServerFactory.java:222)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.createWebServer(ServletWebServerApplicationContext.java:193)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:167)
        ... 31 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'hapiServletRegistration' defined in ca.uhn.fhir.jpa.starter.Application: Unsatisfied dependency expressed through method 'hapiServletRegistration' parameter 0: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:205)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:211)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:202)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.addServletContextInitializerBeans(ServletContextInitializerBeans.java:97)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.<init>(ServletContextInitializerBeans.java:86)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.getServletContextInitializerBeans(ServletWebServerApplicationContext.java:271)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.selfInitialize(ServletWebServerApplicationContext.java:245)
        at org.springframework.boot.web.embedded.tomcat.TomcatStarter.onStartup(TomcatStarter.java:52)
        at org.apache.catalina.core.StandardContext.startInternal(StandardContext.java:4464)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardHost.startInternal(StandardHost.java:772)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardEngine.startInternal(StandardEngine.java:203)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardService.startInternal(StandardService.java:412)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardServer.startInternal(StandardServer.java:870)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.startup.Tomcat.start(Tomcat.java:438)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:128)
        ... 36 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 76 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:388)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1439)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:599)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 90 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'entityManagerFactory' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1806)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:600)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:225)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1328)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1289)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1257)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findDefaultEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:593)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:557)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.resolveEntityManager(PersistenceAnnotationBeanPostProcessor.java:724)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.getResourceToInject(PersistenceAnnotationBeanPostProcessor.java:697)
        at org.springframework.beans.factory.annotation.InjectionMetadata$InjectedElement.inject(InjectionMetadata.java:270)
        at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:145)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:385)
        ... 102 more
Caused by: jakarta.persistence.PersistenceException: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:421)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.afterPropertiesSet(AbstractEntityManagerFactoryBean.java:396)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.afterPropertiesSet(LocalContainerEntityManagerFactoryBean.java:366)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1853)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1802)
        ... 118 more
Caused by: java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at com.zaxxer.hikari.util.DriverDataSource.<init>(DriverDataSource.java:110)
        at com.zaxxer.hikari.pool.PoolBase.initializeDataSource(PoolBase.java:326)
        at com.zaxxer.hikari.pool.PoolBase.<init>(PoolBase.java:112)
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:93)
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112)
        at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:126)
        at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:467)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:46)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:39)
        at org.hibernate.tool.schema.internal.exec.ImprovedExtractionContextImpl.getJdbcConnection(ImprovedExtractionContextImpl.java:63)
        at org.hibernate.tool.schema.extract.spi.ExtractionContext.getQueryResults(ExtractionContext.java:43)
        at org.hibernate.tool.schema.extract.internal.SequenceInformationExtractorLegacyImpl.extractMetadata(SequenceInformationExtractorLegacyImpl.java:39)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.initializeSequences(DatabaseInformationImpl.java:66)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.<init>(DatabaseInformationImpl.java:60)
        at org.hibernate.tool.schema.internal.Helper.buildDatabaseInformation(Helper.java:185)
        at org.hibernate.tool.schema.internal.AbstractSchemaMigrator.doMigration(AbstractSchemaMigrator.java:93)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.performDatabaseAction(SchemaManagementToolCoordinator.java:280)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.lambda$process$5(SchemaManagementToolCoordinator.java:144)
        at java.base/java.util.HashMap.forEach(HashMap.java:1421)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.process(SchemaManagementToolCoordinator.java:141)
        at org.hibernate.boot.internal.SessionFactoryObserverForSchemaExport.sessionFactoryCreated(SessionFactoryObserverForSchemaExport.java:37)
        at org.hibernate.internal.SessionFactoryObserverChain.sessionFactoryCreated(SessionFactoryObserverChain.java:35)
        at org.hibernate.internal.SessionFactoryImpl.<init>(SessionFactoryImpl.java:324)
        at org.hibernate.boot.internal.SessionFactoryBuilderImpl.build(SessionFactoryBuilderImpl.java:463)
        at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:1506)
        at org.hibernate.jpa.HibernatePersistenceProvider.createContainerEntityManagerFactory(HibernatePersistenceProvider.java:142)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.createNativeEntityManagerFactory(LocalContainerEntityManagerFactoryBean.java:390)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:409)
        ... 122 more

[INFO] Running ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest
[INFO] Running ca.uhn.fhir.jpa.starter.common.FhirServerConfigCommonBinaryStorageTest
[INFO] Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.328 s -- in ca.uhn.fhir.jpa.starter.common.FhirServerConfigCommonBinaryStorageTest
[ERROR] Tests run: 4, Failures: 0, Errors: 4, Skipped: 0, Time elapsed: 4.754 s <<< FAILURE! -- in ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest
[ERROR] ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest.testParallelResourceUpdateBundle -- Time elapsed: 0.004 s <<< ERROR!
java.lang.IllegalStateException: Failed to load ApplicationContext for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:180)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
Caused by: org.springframework.context.ApplicationContextException: Unable to start web server
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:170)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:619)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:146)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:755)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:456)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:335)
        at org.springframework.boot.test.context.SpringBootContextLoader.lambda$loadContext$3(SpringBootContextLoader.java:145)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:58)
        at org.springframework.util.function.ThrowingSupplier.get(ThrowingSupplier.java:46)
        at org.springframework.boot.SpringApplication.withHook(SpringApplication.java:1464)
        at org.springframework.boot.test.context.SpringBootContextLoader$ContextLoaderHook.run(SpringBootContextLoader.java:564)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:145)
        at org.springframework.boot.test.context.SpringBootContextLoader.loadContext(SpringBootContextLoader.java:116)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContextInternal(DefaultCacheAwareContextLoaderDelegate.java:225)
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:152)
        ... 17 more
Caused by: org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:147)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.<init>(TomcatWebServer.java:107)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getTomcatWebServer(TomcatServletWebServerFactory.java:520)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getWebServer(TomcatServletWebServerFactory.java:222)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.createWebServer(ServletWebServerApplicationContext.java:193)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:167)
        ... 31 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'hapiServletRegistration' defined in ca.uhn.fhir.jpa.starter.Application: Unsatisfied dependency expressed through method 'hapiServletRegistration' parameter 0: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:205)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:211)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.getOrderedBeansOfType(ServletContextInitializerBeans.java:202)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.addServletContextInitializerBeans(ServletContextInitializerBeans.java:97)
        at org.springframework.boot.web.servlet.ServletContextInitializerBeans.<init>(ServletContextInitializerBeans.java:86)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.getServletContextInitializerBeans(ServletWebServerApplicationContext.java:271)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.selfInitialize(ServletWebServerApplicationContext.java:245)
        at org.springframework.boot.web.embedded.tomcat.TomcatStarter.onStartup(TomcatStarter.java:52)
        at org.apache.catalina.core.StandardContext.startInternal(StandardContext.java:4464)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardHost.startInternal(StandardHost.java:772)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1203)
        at org.apache.catalina.core.ContainerBase$StartChild.call(ContainerBase.java:1193)
        at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
        at org.apache.tomcat.util.threads.InlineExecutorService.execute(InlineExecutorService.java:75)
        at java.base/java.util.concurrent.AbstractExecutorService.submit(AbstractExecutorService.java:145)
        at org.apache.catalina.core.ContainerBase.startInternal(ContainerBase.java:749)
        at org.apache.catalina.core.StandardEngine.startInternal(StandardEngine.java:203)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardService.startInternal(StandardService.java:412)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.core.StandardServer.startInternal(StandardServer.java:870)
        at org.apache.catalina.util.LifecycleBase.start(LifecycleBase.java:164)
        at org.apache.catalina.startup.Tomcat.start(Tomcat.java:438)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:128)
        ... 36 more
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'restfulServer' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: Unsatisfied dependency expressed through method 'restfulServer' parameter 0: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:795)
        at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:542)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1355)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1185)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:562)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 76 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'mySystemDaoR4': Injection of persistence dependencies failed
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:388)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1439)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:599)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:200)
        at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:254)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1448)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1358)
        at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:904)
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:782)
        ... 90 more
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'entityManagerFactory' defined in class path resource [ca/uhn/fhir/jpa/starter/common/StarterJpaConfig.class]: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1806)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:600)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:522)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:337)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:225)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1328)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1289)
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1257)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findDefaultEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:593)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.findEntityManagerFactory(PersistenceAnnotationBeanPostProcessor.java:557)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.resolveEntityManager(PersistenceAnnotationBeanPostProcessor.java:724)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor$PersistenceElement.getResourceToInject(PersistenceAnnotationBeanPostProcessor.java:697)
        at org.springframework.beans.factory.annotation.InjectionMetadata$InjectedElement.inject(InjectionMetadata.java:270)
        at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:145)
        at org.springframework.orm.jpa.support.PersistenceAnnotationBeanPostProcessor.postProcessProperties(PersistenceAnnotationBeanPostProcessor.java:385)
        ... 102 more
Caused by: jakarta.persistence.PersistenceException: [PersistenceUnit: HAPI_PU] Unable to build Hibernate SessionFactory; nested exception is java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:421)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.afterPropertiesSet(AbstractEntityManagerFactoryBean.java:396)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.afterPropertiesSet(LocalContainerEntityManagerFactoryBean.java:366)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1853)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1802)
        ... 118 more
Caused by: java.lang.RuntimeException: Driver org.postgresql.Driver claims to not accept jdbcUrl, jdbc:h2:mem:dbr4
        at com.zaxxer.hikari.util.DriverDataSource.<init>(DriverDataSource.java:110)
        at com.zaxxer.hikari.pool.PoolBase.initializeDataSource(PoolBase.java:326)
        at com.zaxxer.hikari.pool.PoolBase.<init>(PoolBase.java:112)
        at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:93)
        at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112)
        at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:126)
        at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:467)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:46)
        at org.hibernate.resource.transaction.backend.jdbc.internal.DdlTransactionIsolatorNonJtaImpl.getIsolatedConnection(DdlTransactionIsolatorNonJtaImpl.java:39)
        at org.hibernate.tool.schema.internal.exec.ImprovedExtractionContextImpl.getJdbcConnection(ImprovedExtractionContextImpl.java:63)
        at org.hibernate.tool.schema.extract.spi.ExtractionContext.getQueryResults(ExtractionContext.java:43)
        at org.hibernate.tool.schema.extract.internal.SequenceInformationExtractorLegacyImpl.extractMetadata(SequenceInformationExtractorLegacyImpl.java:39)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.initializeSequences(DatabaseInformationImpl.java:66)
        at org.hibernate.tool.schema.extract.internal.DatabaseInformationImpl.<init>(DatabaseInformationImpl.java:60)
        at org.hibernate.tool.schema.internal.Helper.buildDatabaseInformation(Helper.java:185)
        at org.hibernate.tool.schema.internal.AbstractSchemaMigrator.doMigration(AbstractSchemaMigrator.java:93)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.performDatabaseAction(SchemaManagementToolCoordinator.java:280)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.lambda$process$5(SchemaManagementToolCoordinator.java:144)
        at java.base/java.util.HashMap.forEach(HashMap.java:1421)
        at org.hibernate.tool.schema.spi.SchemaManagementToolCoordinator.process(SchemaManagementToolCoordinator.java:141)
        at org.hibernate.boot.internal.SessionFactoryObserverForSchemaExport.sessionFactoryCreated(SessionFactoryObserverForSchemaExport.java:37)
        at org.hibernate.internal.SessionFactoryObserverChain.sessionFactoryCreated(SessionFactoryObserverChain.java:35)
        at org.hibernate.internal.SessionFactoryImpl.<init>(SessionFactoryImpl.java:324)
        at org.hibernate.boot.internal.SessionFactoryBuilderImpl.build(SessionFactoryBuilderImpl.java:463)
        at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:1506)
        at org.hibernate.jpa.HibernatePersistenceProvider.createContainerEntityManagerFactory(HibernatePersistenceProvider.java:142)
        at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.createNativeEntityManagerFactory(LocalContainerEntityManagerFactoryBean.java:390)
        at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:409)
        ... 122 more

[ERROR] ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest.testParallelResourceUpdateNoBundle -- Time elapsed: 0.001 s <<< ERROR!
java.lang.IllegalStateException: ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:145)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)

[ERROR] ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest.testParallelResourceUpdateNoBundleExpectConflict -- Time elapsed: 0.003 s <<< ERROR!
java.lang.IllegalStateException: ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:145)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)

[ERROR] ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest.testParallelResourceUpdateBundleExpectConflict -- Time elapsed: 0.001 s <<< ERROR!
java.lang.IllegalStateException: ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
        at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:145)
        at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:130)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.injectDependencies(DependencyInjectionTestExecutionListener.java:142)
        at org.springframework.test.context.support.DependencyInjectionTestExecutionListener.prepareTestInstance(DependencyInjectionTestExecutionListener.java:98)
        at org.springframework.test.context.TestContextManager.prepareTestInstance(TestContextManager.java:260)
        at org.springframework.test.context.junit.jupiter.SpringExtension.postProcessTestInstance(SpringExtension.java:163)
        at java.base/java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:197)
        at java.base/java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:179)
        at java.base/java.util.ArrayList$ArrayListSpliterator.forEachRemaining(ArrayList.java:1625)
        at java.base/java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:509)
        at java.base/java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:499)
        at java.base/java.util.stream.StreamSpliterators$WrappingSpliterator.forEachRemaining(StreamSpliterators.java:310)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:735)
        at java.base/java.util.stream.Streams$ConcatSpliterator.forEachRemaining(Streams.java:734)
        at java.base/java.util.stream.ReferencePipeline$Head.forEach(ReferencePipeline.java:762)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)

OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 55.28 s -- in ca.uhn.fhir.jpa.starter.MdmTest
[INFO] 
[INFO] Results:
[INFO] 
[ERROR] Errors: 
[ERROR]   CustomBeanTest.testCustomBeanExists » IllegalState Failed to load ApplicationContext for [WebMergedContextConfiguration@66968a15 testClass = ca.uhn.fhir.jpa.starter.CustomBeanTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1,some.custom.pkg2", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.enable_repository_validating_interceptor=true", "hapi.fhir.fhir_version=r4", "hapi.fhir.mdm_enabled=false", "hapi.fhir.cr_enabled=false", "hapi.fhir.subscription.websocket_enabled=false", "spring.main.allow-bean-definition-overriding=true", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@6b7906b3, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@52d239ba, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@3f390d63, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@4e858e0a, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@42f33b5d, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@11981797, org.springframework.boot.test.context.SpringBootTestAnnotation@bbb9a93c], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   CustomInterceptorTest.testAuditInterceptors » IllegalState Failed to load ApplicationContext for [WebMergedContextConfiguration@aae69d3 testClass = ca.uhn.fhir.jpa.starter.CustomInterceptorTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "hapi.fhir.custom-interceptor-classes=some.custom.pkg1.CustomInterceptorBean,some.custom.pkg1.CustomInterceptorPojo", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.cr_enabled=false", "hapi.fhir.fhir_version=r4", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   CustomOperationTest.testCustomOperations » IllegalState Failed to load ApplicationContext for [WebMergedContextConfiguration@7a4154c testClass = ca.uhn.fhir.jpa.starter.CustomOperationTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["hapi.fhir.custom-bean-packages=some.custom.pkg1", "hapi.fhir.custom-provider-classes=some.custom.pkg1.CustomOperationBean,some.custom.pkg1.CustomOperationPojo", "spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.cr_enabled=false", "hapi.fhir.fhir_version=r4", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@64a8c844, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@68ad99fe, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@85e6769, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@7ce97ee5, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@1951b871, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@6b44435b, org.springframework.boot.test.context.SpringBootTestAnnotation@d307348b], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   ParallelUpdatesVersionConflictTest.testParallelResourceUpdateBundle » IllegalState Failed to load ApplicationContext for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   ParallelUpdatesVersionConflictTest.testParallelResourceUpdateBundleExpectConflict » IllegalState ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   ParallelUpdatesVersionConflictTest.testParallelResourceUpdateNoBundle » IllegalState ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[ERROR]   ParallelUpdatesVersionConflictTest.testParallelResourceUpdateNoBundleExpectConflict » IllegalState ApplicationContext failure threshold (1) exceeded: skipping repeated attempt to load context for [WebMergedContextConfiguration@4cfecf7c testClass = ca.uhn.fhir.jpa.starter.ParallelUpdatesVersionConflictTest, locations = [], classes = [ca.uhn.fhir.jpa.starter.Application], contextInitializerClasses = [], activeProfiles = [], propertySourceDescriptors = [], propertySourceProperties = ["spring.datasource.url=jdbc:h2:mem:dbr4", "hapi.fhir.fhir_version=r4", "hapi.fhir.userRequestRetryVersionConflictsInterceptorEnabled=true", "spring.jpa.properties.hibernate.search.backend.directory.type=local-heap", "org.springframework.boot.test.context.SpringBootTestContextBootstrapper=true", "server.port=0"], contextCustomizers = [org.springframework.boot.test.context.filter.ExcludeFilterContextCustomizer@1af687fe, org.springframework.boot.test.json.DuplicateJsonObjectContextCustomizerFactory$DuplicateJsonObjectContextCustomizer@2374d36a, org.springframework.boot.test.mock.mockito.MockitoContextCustomizer@0, org.springframework.boot.test.web.client.TestRestTemplateContextCustomizer@7bb6ab3a, org.springframework.boot.test.web.reactor.netty.DisableReactorResourceFactoryGlobalResourcesContextCustomizerFactory$DisableReactorResourceFactoryGlobalResourcesContextCustomizerCustomizer@3c989952, org.springframework.boot.test.autoconfigure.OnFailureConditionReportContextCustomizerFactory$OnFailureConditionReportContextCustomizer@4bc28c33, org.springframework.boot.test.autoconfigure.actuate.observability.ObservabilityContextCustomizerFactory$DisableObservabilityContextCustomizer@1f, org.springframework.boot.test.autoconfigure.properties.PropertyMappingContextCustomizer@0, org.springframework.boot.test.autoconfigure.web.servlet.WebDriverContextCustomizer@3eeb318f, org.springframework.boot.test.context.SpringBootTestAnnotation@aa085282], resourceBasePath = "src/main/webapp", contextLoader = org.springframework.boot.test.context.SpringBootContextLoader, parent = null]
[INFO] 
[ERROR] Tests run: 13, Failures: 0, Errors: 7, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  01:07 min
[INFO] Finished at: 2025-11-16T13:18:53+05:30
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.4.0:test (default-test) on project hapi-fhir-jpaserver-starter: 
[ERROR] 
[ERROR] Please refer to /media/chandra/b664505e-129c-4c0d-a87b-9efb6469eca2/home/chandra/code/hapi-fhir-jpaserver-starter/target/surefire-reports for the individual test results.
[ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
[ERROR] -> [Help 1]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
chandra@chandra-latitude-ubuntu22:~/code/hapi-fhir-jpaserver-starter$ 