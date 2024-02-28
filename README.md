# Planeamento

Clientes podem reservar os produtos que estão na loja se o produto estiver em stock.  
Administrador pode aceitar ou recusar a reserva. Se aceitar a reserva, o cliente recebe uma notificação para ir buscar o produto na loja e efetuar o pagamento na loja.  
- Os Clientes podem marcar:  
    * Fisioterapia desportiva  
    * Fisioterapia  
    * Reabilitação desportiva   
    * Avaliação postural  
    * Massagem de relaxamento  
    * Massagem descontrotaturante  
    * Drenagem linfática  
    * Knesio taping
       
O administrador pode aceitar ou recusar as marcações, quando aceitar a marcação, o cliente irá receber uma notificação a dizer que foi marcado. 


## Modelo ER

Entidades
```
User(id, username, first_name, last_name, num_telemovel, email, password, is_admin)
Service(id, nome, description, duration, price)
Product(id, name, description, stock, price)
```

Relações
```
ServiceAppointment(id, date, hour, User, Service, status, is_approved, approved_by)
ProductReservation(id, User, Product, status, is_approved, approved_by)
```