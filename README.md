<! DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TO-DO List</title>
  <style>
      body{
          font-family: Arial, sans-serif;
          background-color: #f4f4f4;
          margin: 0;
          display: flex;
          align-items: centre;
          justify-content: center;
          height: 100vh;
      }

      .todo-container{
          background-color: #fff;
          border-radius: 8px;
          box-shadow: 0 0 10px rgba(0,0,0,0.1);
          width: 300px;
          padding: 20px;
        }

        .todo-header{
            text-align: centre;
            font-size: 24px;
            margin-bottom: 20px;
        }

        .todo-list{
            list-style-type: none;
            padding: 0;
        }

        .todo-item{
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px;
            border-bottom: 1px solid #ccc;
        }

        .todo-item input{
             margin-right: 10px;
        }

        .todo-item button{
            background-color: #e74c3c;
            color: #fff;
            border: none;
            padding: 8px 12px;
            cursor: pointer;
        }

        .todo-item button:hover{
            background-color: #c0392b;
        }
      </style>
    </head>
    <body>

    <div class="todo-container">
         <div class="todo-header">TO-DO List</div>
         <ul class="todo-list" id="todolist">
             <!-- TO-DO items will be added here dynamically using javascript -->
         </ul>
         <div>
            <input type="text" id="newTodo" placeholder="Add a new task">
            <button onclick="addTOdo()">Add</button>
         </div>
       </div>

       <script>
           function addTodo(){
                const todoList= document.getElementById("todoList");
                const newTodoInput=document.getElementById("newTodo");

                if(newTodoInput.value.trim() !-- "") {
                   const li= document.createElement("li");
                   li.className= "todo-item";
                   li.innerHTML=
                      <input type="checkbox">       
                      <spans>${newTodoInput.value}</span>
                       <button onclick="removeTodo(this)">Remove</button>
                   ;
                   todoList.appendChild(l1);
                   newTodoInput.value="";
              }
          }

          function removeTodo(button){
              const todoItem=button.parentElement;
              todoItem.remove();
            }
        </script>

        </body>
        </html>
                       
                      
        
