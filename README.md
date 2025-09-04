@PostMapping(*/add*)
public ResponseEntity <Employee> createEmployee(@RequestEody Employee employee) [
Employee savedEmployee = employeeService. saveEmployee(employee);
return ResponseEntity.ok(savedEmployee);
@GetMapping(*/{id}")
public Responseintity«Employee> getEmployeeById(@PathVariable Long id) f
Optional‹Employee> employee = employeeService•getEmployeeById(1d);
return employee.map(ResponseEntity: :ok) •orElseGet(() -> ResponseEntity.notFound().bufld()):
@GetMapping(*/all")
public ResponseEntity«List<Employee>> getAllEmployees( (
List«Employee> employees - employeeService.getAllEmployees();
return ResponseEntity.ok (employees);
@PutMapping(*/update/{id)°)
public ResponseEntity«Employee> updateEmployee@PathVariable Long id, @RequestBody Employee employeeDetails) (
Optional«Employee> updatedEmployee = employeeService.updateEmployee(id, employeeDetails); return updatedEmployee.map(ResponseEntity: :ok).0rElseGet(() -> ResponseEntity.notFound().bulld()):
