# cqrs-demo
event-driven-microservices

# Run axon server in docker
docker run -d --name axonserver -p 8024:8024 -p 8124:8124 -e AXONIQ_AXONSERVER_STANDALONE=true axoniq/axonserver:latest

# Create a product
curl --location 'http://localhost:8081/products' \
--header 'Content-Type: application/json' \
--data '{
    "name": "apple",
    "price": "500",
    "quantity": "50"
}'

# Get all products
curl --location 'http://localhost:8081/products'