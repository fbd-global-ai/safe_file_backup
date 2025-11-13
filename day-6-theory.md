import os 
from datetime import datetime


def get_file_info(path):
    try:
        files = os.listdir(path):
    except FileNotFoundError:
         print("Path not found!")
         return
        
         report = []

         for file in files
            full_path = os.path.join(parh, file) 

            if os.path.isfile(full_path):
                size = os.path.getsize(full_path)
                ext = os.path.getsize(full_path)
                creadet_at =datetime.fromtimestamp(os.path.getctime(full_path))

                report.append({
                    "name": file,
                    "extension":ext,
                    "size_kb":round(size / 1024, 2),
                    "created": creadet_at
                    })

                    return report

              def print_report(report):
                  for item in report:
                  print(f"File: {item['name']}")
                  print(f" - Extension: {item['extension']}")
                  print(f" - Size(KB): {item['sıze_kb']}")
                  print(f" - Created: {item['creadet']}")
                  print("-" * 30) 
              # Main excution
              if __name__== "__main__":
                path =input(Enter folder path: ")
                result =get_file_info(path)
                if result:
                  print report(result) 
         
    
