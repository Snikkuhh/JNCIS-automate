# Challenge 16 – GRE over IPsec (Route-Based)

## ✅ Status: Partially Completed

This challenge aimed to create a route-based IPsec VPN with a GRE tunnel between vMX1 and vMX2 using Junos.

---

## 🧪 Attempted Configuration

- `st0.0` interface configured with family `inet`
- IKE proposals, policies, gateways set correctly
- IPsec proposals and policy created
- GRE IP planned through the IPsec tunnel

---

## ❌ Lab Limitation

This challenge could **not be fully completed** due to platform limitations on vMX:

- `ipsec vpn` configuration is **not supported** (command not recognized)
- `security forwarding-options` is **not available**
- `st0.0` does **not activate** due to missing forwarding engine
- IPsec VPN binding fails due to lack of feature support

---

## 🔧 Recommendation

To fully complete this challenge:

- Use **vSRX** instead of vMX (e.g. in EVE-NG or vLabs)
- Alternatively, simulate GRE without encryption

---

## 📌 Marked as:
```diff
- Partially complete (GRE working, IPsec not possible on current image)