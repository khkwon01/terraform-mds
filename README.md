# terraform-mds

Provision MySQL Database Service (MDS) and Heatwave with Terraform.

[![Deploy to Oracle Cloud](https://oci-resourcemanager-plugin.plugins.oci.oraclecloud.com/latest/deploy-to-oracle-cloud.svg)](https://cloud.oracle.com/resourcemanager/stacks/create?zipUrl=https://github.com/khkwon01/terraform-mds/archive/refs/tags/mds-heatwave-v1.3.0.zip)


# demo diagram
If you execute the above terraform code in oci, it make the below service like diagram which the heatwave node is disabled.
<img width="802" alt="image" src="https://user-images.githubusercontent.com/8789421/213102145-3a14870d-7a6a-4a54-a1fb-d2eee02c4d58.png">

# demo scenario
- HeatWave : https://apexapps.oracle.com/pls/apex/r/dbpm/livelabs/run-workshop?p210_wid=3157
- ML : https://apexapps.oracle.com/pls/apex/r/dbpm/livelabs/run-workshop?p210_wid=3306&p210_wec=&session=374748331881
  - When the function of ML_PREDICT_ROW, ML_EXPLAIN_ROW have some errors, use the below function arguement..
    - SELECT sys.ML_PREDICT_ROW(@row_input, @iris_model, JSON_OBJECT('prediction_explainer', 'permutation_importance'));
    - SELECT sys.ML_EXPLAIN_ROW(@row_input, @iris_model, JSON_OBJECT('prediction_explainer', 'permutation_importance'));
