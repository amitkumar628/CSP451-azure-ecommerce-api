# CSP451-azure-ecommerce-api
Serverless E-Commerce API using Azure Functions
Azure Serverless E-Commerce API
📋 Project Overview
A complete serverless e-commerce API built with Azure Functions, featuring product catalog, order management, and payment processing.

Student: Amit Kumar
Student ID: 153260237
Course: CSP451 - Cloud Computing
Email: akumar250@myseneca.ca

🚀 Live Deployment
Base URL: https://ecommfunc153260237.azurewebsites.net

📊 API Endpoints
1. Get Products
http
GET /api/products
GET /api/products/{id}
Response:

json
{
  "success": true,
  "products": [
    {
      "id": "1",
      "name": "Azure T-Shirt",
      "price": 25.99
    }
  ]
}
2. Create Order
http
POST /api/orders
Request:

json
{
  "product_id": "1",
  "quantity": 2,
  "customer_name": "Amit Kumar",
  "customer_email": "akumar250@myseneca.ca"
}
3. Process Order
http
POST /api/orders/{orderId}/process
Response:

json
{
  "success": true,
  "result": {
    "order_id": "abc123-def456",
    "status": "processed",
    "payment": "confirmed",
    "tracking": "TRACK123456",
    "delivery": "2025-11-12"
  }
}
🏗️ Architecture
Azure Services Used
Azure Functions - Serverless API endpoints (Python 3.11)

Azure Blob Storage - Product catalog and order data storage

Azure Service Bus - Order processing queue

Function Authentication - Secure API access

Data Flow
Client → HTTP Request → Azure Functions

Functions → Read/Write → Blob Storage

Functions → Queue Messages → Service Bus

Functions → Return JSON Response → Client

💰 Cost Analysis
Monthly Operational Costs
Service	Cost
Azure Functions	$0.00 (Free Tier)
Blob Storage	$0.02
Service Bus	$0.05
Total	$0.07
Traditional vs Serverless
Solution	Monthly Cost	Annual Cost
Traditional Hosting	$97.67	$1,172.04
Azure Serverless	$0.07	$0.84
Savings	99.9%	99.9%
Free Tier Utilization
✅ 1M Azure Function executions/month

✅ 5GB Blob Storage + 10K operations

✅ 1M Service Bus operations

✅ 100% of POC usage covered by free tier

🔧 Technical Features
Serverless Architecture - Zero infrastructure management

Automatic Scaling - Handles 0 to millions of requests

Tax Calculation - Automatic 13% HST for Ontario

Payment Processing - Simulated payment gateway

Order Tracking - Automated tracking numbers

RESTful API - JSON responses with proper status codes

🚀 Deployment Details
Azure Resources
Resource Group: Student-RG-1887890

Region: Canada East

Function App: ecommfunc153260237

Storage: ecommstore153260237

Service Bus: ecommbus153260237

Deployment Commands
bash
# Deploy to Azure
func azure functionapp publish ecommfunc153260237 --python
🧪 Testing
Test Commands
bash
# Get all products
curl "https://ecommfunc153260237.azurewebsites.net/api/products?code=YOUR_KEY"

# Create order
curl -X POST "https://ecommfunc153260237.azurewebsites.net/api/orders?code=YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"product_id": "1", "quantity": 2, "customer_name": "Test User"}'
📈 Business Value
95% Cost Reduction vs traditional hosting

Zero Infrastructure Management - No servers to maintain

Automatic Scaling - Handles traffic spikes automatically

Rapid Deployment - Deployed in under 3 hours

Enterprise Reliability - 99.95% SLA from Microsoft

🔮 Future Enhancements
Azure Cosmos DB for global distribution

Azure CDN for faster content delivery

Application Insights for advanced monitoring

Real payment gateway integration (Stripe/PayPal)

Azure API Management for rate limiting

📞 Support
For questions or issues, contact:
Amit Kumar
akumar250@myseneca.ca

Last Updated: November 2025
Azure Region: Canada East
*Course: CSP451 - Cloud Computing, Seneca College*
