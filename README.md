# Oracle ERP Cloud Business Event Subscription – OIC Integration

This project demonstrates how to subscribe to Oracle ERP Cloud business events (like Purchase Order Created, Invoice Approved, etc.) and process them using Oracle Integration Cloud (OIC).

## 🚀 Use Case

- Automatically process ERP Cloud business events using Oracle Integration Cloud
- Send event payloads to third-party apps or perform downstream tasks
- Monitor, transform, or log events in real-time

## 🧰 Technologies Used

- Oracle Integration Cloud (OIC)
- Oracle ERP Cloud Adapter
- Business Events Framework (ERP Cloud)
- REST APIs / SOAP Services
- JSON / XSLT

## 📦 Project Artifacts

| File | Description |
|------|-------------|
| `event-subscription-integration.iar` | OIC integration archive |
| `sample-event-payload.json` | Sample event data from ERP Cloud |
| `setup-guide.md` | How to enable and test the integration |
| `project-description.md` | High-level use case and architecture |
| `event-subscription-architecture.png` | Integration architecture diagram |

## 🛠️ How to Deploy

1. Import `event-subscription-integration.iar` into your OIC instance
2. Configure ERP Cloud Adapter with correct connection credentials
3. Subscribe to Business Event in ERP (via FSM or web services)
4. Deploy the integration and test using mock or real events

## 📧 Sample Event: PO Created

```json
{
  "eventName": "oracle.apps.prc.po.events.public.PurchaseOrderHeaderEvent",
  "eventKey": "300000123456789",
  "eventData": {
    "PurchaseOrderNumber": "PO-123456",
    "Supplier": "ABC Supplies",
    "Amount": 5000
  }
}
