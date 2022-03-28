# Lab4-TiMP



```
name: Formatter_application

on:
  push:
      branches: 
      - master
  
jobs:
  Libraries:
  
    runs-on: ubuntu-latest
    
    steps:
      - uses: actions/checkout@v2
 
      - name: formatter_lib
        shell: bash
        run: |
          cd formatter_lib
          cmake -H. -B_build
          cmake --build _build
          
      - name: formatter_ex_lib
        shell: bash
        run: |
         cd formatter_lib
         cmake -H. -B_build
         cmake --build _build 
         
      - name: solver_lib
        shell: bash
        run: |
          cd solver_lib
          cmake -H. -B_build
          cmake --build _build
      
  Build_Hello_World_App:
     
        runs-on: ubuntu-latest
        
        steps:
          - uses: actions/checkout@v2
        
          - name: Hello_world_build
            shell: bash
            run: |
              mkdir hello_world
              cd hello_world
              cmake ..
              cmake --build .
              
          - name: text_output
            shell: bash
            run: |
              cd hello_world/hello_world_application
              ./hello_world
              
  Build_Solver_App:
        
        runs-on: ubuntu-latest
        
        steps:
          - uses: actions/checkout@v2
          
          - name: Solver_build
            shell: bash
            run: |
              mkdir solver
              cd solver
              cmake ..
              cmake --build .
              
          - name: solver_output
            shell: bash
            run: |
              cd solver/solver_application
              ./equation 1 5 6
```
