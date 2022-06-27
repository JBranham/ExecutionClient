# ToscaExecutionClient

http://localhost:90/automationobjectservice/swagger/index.html

https://github.com/Tricentis/ToscaExecutionClient

      - task: PowerShell@2
        inputs:
          filePath: $(System.DefaultWorkingDirectory)\tosca_execution_client.ps1
          arguments: >
            -toscaServerUrl "http://localhost:5012"
            -projectName "DEX_User"
            -eventsConfigFilePath "testEvents.json"
            -clientId "jFoM6R2JeES2QX-yimEfYg"
            -clientSecret "yzrpQKziLEqQb-EsK3_tLAcwZU_FiYCEC3BYurGd_g4A"
            -creator "ToscaExecutionClient ADO Pipeline"
            -resultsFileName "results.xml"
            -resultsFolderPath "results"
            -debug "true"
        displayName: 'Execute Tosca TestEvent(s) via ToscaExecutionClient and Upload Results to qTest'
