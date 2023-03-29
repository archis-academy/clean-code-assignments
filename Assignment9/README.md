# clean-code-assignments

9.Avoid long functions and break them up into smaller functions: Functions should be short and do one thing only. If a function is too long, break it up into smaller functions that perform specific tasks.

Suppose you have a function that calculates the total price of an order based on the quantity and unit price of the items in the order. However, this function also handles updating the inventory and generating an invoice for the order, making it too long and complicated.

Here's an example of breaking up this function into smaller, more focused functions:

```
// Original function
function calculateOrderTotal(order) {
  // Update inventory
  for (let i = 0; i < order.items.length; i++) {
    updateInventory(order.items[i]);
  }

  // Calculate total price
  let totalPrice = 0;
  for (let i = 0; i < order.items.length; i++) {
    let item = order.items[i];
    totalPrice += item.quantity * item.unitPrice;
  }

  // Generate invoice
  let invoice = generateInvoice(order, totalPrice);

  // Return total price and invoice
  return { totalPrice, invoice };
}

// Updated function using smaller functions

function calculateOrderTotal(order) {
  updateInventory(order.items);
  let totalPrice = calculateTotalPrice(order.items);
  let invoice = generateInvoice(order, totalPrice);
  return { totalPrice, invoice };
}

function updateInventory(items) {
  for (let i = 0; i < items.length; i++) {
    let item = items[i];
    // Update inventory for this item
  }
}

function calculateTotalPrice(items) {
  // code for calculate total price
}

```

Question : write a function that calculates the total price of an order based on the quantity and unit price of the items in the order
