Envoy


Access Logs

Listerner > Route > Cluster

istioctl proxy-status

istioctl dashboard envoy daemonset.apps/istio-ingressgateway.istio-system

>> Get the list of listerners (IP + PORT)
istioctl proxy-config listener -n istio-system daemonset.apps/istio-ingressgateway

ADDRESSES PORT  MATCH                                             DESTINATION
0.0.0.0   8443  SNI: abc.example.com Route: https.443.default-gatewayport443.<gateway>.<namespace>

Get the list of routes
istioctl proxy-config route -n istio-system daemonset.apps/istio-ingressgateway

Route: https.443.default-gatewayport443.<gateway>.<namespace>
