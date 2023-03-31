# Order Management API

A restApi for creating, reading and updating orders

## Instructions

Install all required dependencies

```bash
npm install
```

Create a .env file: "/backend/.env"
Add the Database URI and PORT in this format:

```bash
PORT = 4000
DB_URI = "mongodb://localhost:27017/Orders"
```

## Run the server

run the following command

```bash
cd backend
npm run dev
```

## API Endpoints

```bash
# ORDER ENDPOINTS

| HTTP Request |    Endpoint    |             Action            |
|:------------:|:--------------:|:-----------------------------:|
| GET          | /api/orders    | To view all orders            |
| POST         | /api/order/new | To create a new order         |
| PUT          | /api/order/:id | To update the status of order |


# PRODUCT ENDPOINTS

| HTTP Request |     Endpoint     |          Action          |
|:------------:|:----------------:|:------------------------:|
| GET          | /api/products    | To view all products     |
| POST         | /api/product/new | To create a new product  |


#TRIP ENDPOINTS

| HTTP Request |    Endpoint   |         Action        |
|:------------:|:-------------:|:---------------------:|
| GET          | /api/trips    | To view all trips     |
| POST         | /api/trip/new | To create a new trip  |

```

## Sample

### An example of Order

```json
{
  "senderLocation": {
    "coordinates": [122, 20],
    "type": "Point"
  },
  "receiverLocation": {
    "coordinates": [122, 20],
    "type": "Point"
  },
  "_id": "642087932e4ac98ddaa85cde",
  "senderName": "Sender-1",
  "receiverName": "Receiver-1",
  "orders": [
    {
      "length": 1,
      "breadth": 1,
      "height": 1,
      "weight": 1,
      "productItems": [
        {
          "item": "6420595ed99f4774a4d90d19",
          "quantity": 5,
          "_id": "642087932e4ac98ddaa85ce0"
        },
        {
          "item": "6420549051c28e0a34378bcc",
          "quantity": 2,
          "_id": "642087932e4ac98ddaa85ce1"
        }
      ],
      "_id": "642087932e4ac98ddaa85cdf"
    }
  ],
  "trips": [
    {
      "trip": "64205f708f2307825d11f5a2",
      "_id": "642087932e4ac98ddaa85ce2"
    },
    {
      "trip": "64205f858f2307825d11f5a4",
      "_id": "642087932e4ac98ddaa85ce3"
    }
  ]
}
```

### An example of Product

```json
{
  "_id": "6420549051c28e0a34378bcc",
  "name": "product-1",
  "price": 1200,
  "imageUrl": "URL-1"
}
```

### An example of Trip

```json
{
  "startLocation": {
    "coordinates": [122, 22],
    "type": "Point"
  },
  "endLocation": {
    "coordinates": [122, 22],
    "type": "Point"
  },
  "_id": "64205f858f2307825d11f5a4",
  "shipperName": "Shipper-2",
  "tripStatus": "Out for delivery"
}

// "tripStatus":['Not Started', 'Out for Pickup', 'In transit', 'Out for delivery', 'Delivered']
```
