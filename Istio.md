Envoy


Access Logs

istioctl proxy-status

istioctl dashboard envoy daemonset.apps/istio-ingressgateway.istio-system

**Listerner > Route > Cluster**


**Get the list of listerners (IP + PORT)**
istioctl proxy-config listener -n istio-system daemonset.apps/istio-ingressgateway

ADDRESSES PORT  MATCH                                             DESTINATION
0.0.0.0   8443  SNI: abc.example.com                              Route: https.443.default-gatewayport443.<gateway>.<namespace>

**Get list of routes**
istioctl proxy-config route -n istio-system daemonset.apps/istio-ingressgateway

Route: https.443.default-gatewayport443.<gateway>.<namespace>

**Get list of clusters**
istioctl proxy-config cluster -n istio-system daemonset.apps/istio-ingressgateway
istioctl proxy-config clusters <pod-name[.namespace]> --port 9080

**Get list of endpoints**
istioctl proxy-config endpoint -n istio-system daemonset.apps/istio-ingressgateway
