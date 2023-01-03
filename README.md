# sso-openshift-persistent-postgresql

https://developers.redhat.com/blog/2021/02/19/x-509-user-certificate-authentication-with-red-hats-single-sign-on-technology

https://access.redhat.com/solutions/5162701

https://access.redhat.com/documentation/en-us/red_hat_single_sign-on/7.5/html/red_hat_single_sign-on_for_openshift/index

https://github.com/jboss-container-images/redhat-sso-7-openshift-image/tree/sso75-dev

oc process -f templates/sso75-postgresql.json -p HTTPS_SECRET="sso-app-secret"  -p HTTPS_KEYSTORE="sso.jks"  -p HTTPS_NAME="jboss"  -p HTTPS_PASSWORD="http-pass"  -p JGROUPS_ENCRYPT_SECRET="sso-app-secret"  -p JGROUPS_ENCRYPT_KEYSTORE="jgroups.jceks"  -p JGROUPS_ENCRYPT_NAME="jgroups"  -p JGROUPS_ENCRYPT_PASSWORD="jgroups-pass"  -p SSO_ADMIN_USERNAME="admin"  -p SSO_ADMIN_PASSWORD="admin-pass"  -p SSO_REALM="test-realm"  -p SSO_TRUSTSTORE="truststore.jks"  -p SSO_TRUSTSTORE_PASSWORD="truststore-pass"  -p SSO_TRUSTSTORE_SECRET="sso-app-secret" -o yaml > ~/sso/everything.yaml
