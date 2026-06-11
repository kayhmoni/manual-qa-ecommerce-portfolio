# API Testing Checklist

Use Postman to practice API testing with Restful Booker or ReqRes.

## Common API Checks

- Verify correct status code: 200, 201, 400, 401, 404, 500
- Verify response body contains expected fields
- Verify response time is acceptable
- Verify required fields cannot be omitted
- Verify invalid data returns a clear error
- Verify unauthorized requests are rejected
- Verify created data can be retrieved
- Verify updated data is saved correctly
- Verify deleted data is no longer available

## Example Test Scenarios

| ID | Method | Endpoint Type | Scenario | Expected Result |
|---|---|---|---|---|
| API-001 | GET | List records | Retrieve all users/bookings | Status 200 and list is returned |
| API-002 | GET | Single record | Retrieve valid record by ID | Status 200 and correct record is returned |
| API-003 | GET | Single record | Retrieve invalid record ID | Status 404 or clear error response |
| API-004 | POST | Create record | Submit valid request body | Status 200/201 and new record is created |
| API-005 | POST | Create record | Submit missing required field | Status 400 or validation error |
| API-006 | PUT | Update record | Update existing record | Status 200 and changes are saved |
| API-007 | DELETE | Delete record | Delete existing record | Status 200/204 and record is removed |
| API-008 | Auth | Protected endpoint | Send request without token | Status 401 or 403 |

## Postman Test Examples

```javascript
pm.test("Status code is 200", function () {
  pm.response.to.have.status(200);
});

pm.test("Response time is below 1000ms", function () {
  pm.expect(pm.response.responseTime).to.be.below(1000);
});

pm.test("Response has expected field", function () {
  const jsonData = pm.response.json();
  pm.expect(jsonData).to.have.property("id");
});
```

