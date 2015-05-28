# streamsx.spss.v4
###Toolkit for working with SPSS  in SPL applications.

The SPSS Analytics Toolkit contains InfoSphere Streams1 operators that integrate with IBM SPSS Modeler2 and SPSS Collaboration and Deployment Services3 products to implement various aspects of SPSS Modeler predictive analytics in your InfoSphere Streams applications:

- SPSSScoring operator - integrates with SPSS Modeler Solution Publisher to the enable the scoring of your SPSS Modeler designed predictive models in InfoSphere Streams applications
- SPSSPublish operator - automates the SPSS Modeler Solution Publisher ‘publish’ function which generates the required executable images needed to refresh the model used in your InfoSphere Streams applications from the logical definition of an SPSS Modeler scoring branch defined in a SPSS Modeler file
- SPSSRepository operator - detects notification events indicating changes to the deployed models managed in the SPSS Collaboration and Deployment Services repository and retrieves the indicated Modeler file version for automated publish and preparation for use in your InfoSphere Streams applications

The granularity of the operators implemented in this toolkit enable the following basic implementation strategies:

- SPSSScoring operator only in the Streams application – site management of changes to SPSS Modeler files used in application placing ‘promotion’ and related ‘publish’ of updated models outside of InfoSphere Streams application domain
- SPSSScoring plus SPSSPublish operators used in the Streams application – site manages SPSS Modeler file versions outside of stream application but leverages of automation of ‘publish’ functionality refreshing the models used in deployed stream applications
- SPSSScoring, SPSSPublish and SPSSRepository operators all used in Streams application – SPSS Modeler assets managed in SPSS Collaboration and Deployment Services repository, InfoSphere Streams application refreshes the Modeler files used by its operators while jobs executing. All download, publish and refresh automation based on promotion event notifications issued from the SPSS Collaboration and Deployment Services repository.

----
Installing the SPSS Analytics Toolkit
----
The following SPSS Analytics Toolkit install assets can be found in this repository.

1. The SPSS Analytics Toolkit for InfoSphere Streams toolkit installation archive SpssAnalyticsToolkit.tar.gz
2. The toolkit installation helper script installToolkit.sh
2. A readme file that describes

---
License
----

[Apache 2.0][1]

[1]: http://www.apache.org/licenses/LICENSE-2.0.html


