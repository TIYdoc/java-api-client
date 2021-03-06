java-api-client
===============

Kiuwan Java client for REST API.

Maven configuration:

	<dependency>
		<groupId>com.kiuwan</groupId>
		<artifactId>java-api-client</artifactId>
		<version>0.0.4</version>
	</dependency>
	
Supported actions are: (New actions are marked with (*))

  - List your applications.
  - Get last analysis results from your application.
  - Get all defects from your application.
  - Get files (with metric values and defects) from your application.
  - Get all defects from your application indicating the analysis code.
  - Get files (with metric values and defects) from your application indicating the analysis code.
  - Get the differences of defects between two analysis.
  - Create new applications. (*)
  - Create new users in your account. (*)
  - Delete applications. (*)
  - Delete users of your account. (*)
  - Modify applications' information. (*)
  - Modify users' information. (*) 
  
Source code includes examples that shows you how to execute each supported action. (New examples are marked with (*))

  - <a href="src/main/java/com/kiuwan/client/examples/ListApplications.java">com.kiuwan.client.examples.ListApplications.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/ApplicationsResults.java">com.kiuwan.client.examples.ApplicationsResults.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/ApplicationDefects.java">com.kiuwan.client.examples.ApplicationDefects.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/ApplicationFiles.java">com.kiuwan.client.examples.ApplicationFiles.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/AnalysisDefects.java">com.kiuwan.client.examples.AnalysisDefects.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/AnalysisFiles.java">com.kiuwan.client.examples.AnalysisFiles.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/CompareAnalysisDefects.java">com.kiuwan.client.examples.CompareAnalysisDefects.java</a>
  - <a href="src/main/java/com/kiuwan/client/examples/CreateApplications.java">com.kiuwan.client.examples.CreateApplications.java</a> (*) 
  - <a href="src/main/java/com/kiuwan/client/examples/CreateUsers.java">com.kiuwan.client.examples.CreateUsers.java</a> (*) 
  - <a href="src/main/java/com/kiuwan/client/examples/DeleteApplications.java">com.kiuwan.client.examples.DeleteApplications.java</a> (*) 
  - <a href="src/main/java/com/kiuwan/client/examples/DeleteUsers.java">com.kiuwan.client.examples.DeleteUsers.java</a> (*)
  - <a href="src/main/java/com/kiuwan/client/examples/ModifyApplications.java">com.kiuwan.client.examples.ModifyApplications.java</a> (*)
  - <a href="src/main/java/com/kiuwan/client/examples/ModifyUsers.java">com.kiuwan.client.examples.ModifyUsers.java</a> (*)

Example of use:

	KiuwanRestApiClient client = new KiuwanRestApiClient(username, password);

	try {
		List<Application> apps = client.getApplications();
		for(Application app: apps) {
			System.out.println(app);
		}
		
	} catch (KiuwanClientException e) {
		e.printStackTrace();
	}

