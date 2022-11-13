# replaceSvgColorUseCsv

Produces SVG Logo Versions given a directory containing the following:
- findAndReplaceSvg.js
- SVG Files
- a CSV containing the following columns:
  new_file, original_file, find1, replace1


 PARAMETERS
   __________
   
   --csv_matcher
        - default: Replace
        - required: false
        - A continuous string (endss at first white space)
          from which a new regular expression is created and 
          used to find a CSV file in the containing directory
        - example - If you want use a CSV with filename "finreplac123.csv",
          you could run the following command.
          $ node findAndReplaceSvg --csv_matcher finrep
   
   --out_dir
        - default: _OUT
        - required: false
        - Name of output directory, which will be created in containing directory.
        - example - To generate output files in "/SVGS_OUTPUT/", run the follwing command.
          $ node findAndReplaceSvg --out_dir SVGS_OUTPUT
   
   --prod
        - Remove this documentation from console.log output
        - example - Run the follwing command.
          $ node findAndReplaceSvg --prod
   
   
    CSV SPECIFICATIONS:
            
        REQUIRED COLUMNS (COLUMN HEADERS MUST MATCH)
   
            - new_file
            - original_file
            - find1
            - replace1
        
            - *OPTIONAL find2
            - *OPTIONAL replace2
            - *OPTIONAL find3
            - *OPTIONAL replace3
