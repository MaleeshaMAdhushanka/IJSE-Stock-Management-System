# TestJava
import java.util.*;
public class pp{
	private static String []pred={"mal","1234"};
	private static Scanner input = new Scanner(System.in);
	private static String[] supplierIds = new String[1];
    private static String[] supplierNames = new String[1];
    private static int numSuppliers = 0;
    private static String[] itemCategories = new String[1];
    private static int itemCount = 0;
    private static String[] items = new String[1];
    private static int numitem = 0;
	private static String[][] SuppItem = new String[1][3];
	private static int countz = 0;
	private static String[][] itemdetails =new String[numitem][2];
	private static int itemDetailCount =0;
	private static float[] price = new float[1];
	private static int priceCount = 0;
	
	public static String[] usernamepassword(){
	System.out.println("\t\t\t\t+--------------------------------------------------------+");
	System.out.println("\t\t\t\t|                      LOGIN PAGE                        |");
	System.out.println("\t\t\t\t+--------------------------------------------------------+");

		System.out.println();
		
		while(true){
			System.out.print("\n"+"User Name : ");
			String inputusername = input.nextLine();
				if(pred[0].equals(inputusername)){
				while(true){
					System.out.print("\n"+"Password  : ");
					String inputpassword= input.nextLine();
					if(pred[1].equals(inputpassword)){
						break;
					}else{
						System.out.print("password is incorrect. please try again!"+"\n");
						}
					}
					break;
					}else{
						System.out.print("user name is invalid. please try again!"+"\n");
						}
			}
			return pred;
			
}

	public static void stockManagement(){
		System.out.println("\t\t\t\t+-------------------------------------------------------------+");
		System.out.println("\t\t\t\t|             WELCOME TO IJSE STOCK MANAGEMENT SYSTEM         |");
		System.out.println("\t\t\t\t+-------------------------------------------------------------+");
		System.out.println();
		System.out.print("[1]Change The Credentials");
		System.out.println("\t\t\t[2]Supplier Manage");
		System.out.print("[3]Stock Manage");
		System.out.println("\t\t\t\t\t[4]Log out");
		System.out.println("[5]Exit the System");
		System.out.println();
		stockManagementOption();
	}
	
	public static void clearConsole() {
        try {
            final String os = System.getProperty("os.name");

            if (os.contains("Windows")) {
                // For Windows
                new ProcessBuilder("cmd", "/c", "cls").inheritIO().start().waitFor();
            } else {
                // For Unix/Linux/MacOS
                System.out.print("\033[H\033[2J");
                System.out.flush();
            }
        } catch (final Exception e) {
            // Handle exceptions if any
            System.out.println("Error while clearing console: " + e.getMessage());
        }
    }
	public static void changeTheCredentials(){
	Scanner input = new Scanner(System.in);
	
		System.out.printf("\t\t\t+---------------------------------------------------------------------------------+%n");
		System.out.printf("\t\t\t|\t\t                     CREDENTIAL MANAGE                            |%n");
		System.out.printf("\t\t\t+---------------------------------------------------------------------------------+%n"+"\n");
		
		while(true){
			System.out.print("Please enter the user name to verify it's you: ");  
			String UserName = input.nextLine();
				if(pred[0].equals(UserName)){
					System.out.print("Hey "+pred[0]+"\n");
					
					while(true){
					System.out.print("Enter your current password: ");
					String inputpassword = input.nextLine();
					
						if(pred[1].equals(inputpassword)){
							System.out.print("Enter your new password: ");
							String NewUserName = input.nextLine();
							pred[0]=NewUserName;
								System.out.print("\n"+"Password changed successfully!"+" Do you want to go home page (Y/N):");
								char x = 'y';
								char y = 'Y';
								char YesNo = input.next().charAt(0);
									if(x==YesNo){
										clearConsole();
										stockManagement();
										}
										
										if(y==YesNo){
										clearConsole();
										stockManagement();
										}
										
										else{
											System.out.print("See you...Come again!");
											
										}return;
						}
						System.out.print("incorrect password. try again!"+"\n"+"\n");
					}
				}else{
				System.out.print("invalid user name. try again!"+"\n"+"\n");
				}
		}
			
			
	}
	public static void StockManage(){
		Scanner input = new Scanner(System.in);
		System.out.println("\t\t\t\t+--------------------------------------------------------+");
		System.out.println("\t\t\t\t|                     STOCK MANAGEMENT                   |");
		System.out.println("\t\t\t\t+--------------------------------------------------------+");
		System.out.println();
		System.out.print("[1]Manage Item Categories");
		System.out.println("\t\t\t[2]Add Item");
		System.out.print("[3]Get items supplier wise");
		System.out.println("\t\t\t[4]View items");
		System.out.print("[5]Rank items per unit price");
		System.out.println("\t\t\t[6]Home page");
		System.out.println();
		
		System.out.print("Enter an option to continue->");
		int num1 = input.nextInt();
		
		
		if (num1==1){
			clearConsole();
			ManageItemCategories();
			}
		if (num1==2)
		{
			clearConsole();
			addItem();
		}
		if (num1==3)
		{
			clearConsole();
			getItems();
		}
		if (num1==4)
		{
			clearConsole();
			viewItem();
		}
		if (num1==5)
		{
			clearConsole();
			rankItem();
		}
		if (num1==6)
		{
			clearConsole();
			stockManagement();
		}
		
	}
	public static void logout(){
		clearConsole();
		usernamepassword();
	}
	public static void exitTheSystem(){

	}
	public static void homepage(){

	}	
    public static void stockManagementOption(){
		System.out.print("Enter an option to continue->");
		int num=input.nextInt();
		if (num==1)
		{
		clearConsole();
		changeTheCredentials();
		}
		if (num==2)
		{
		clearConsole();
		SupplierManage();
		}
		if (num==3)
		{
		clearConsole();
		StockManage();
		}
		if (num==4)
		{
		clearConsole();
		logout();
		}
		if (num==5)
		{
		clearConsole();
		exitTheSystem();
		}
		if (num==6)
		{
		clearConsole();
		stockManagement();
		}

	}
	public static void ManageItemCategories(){
		Scanner input = new Scanner(System.in);
		System.out.printf("\t\t\t+---------------------------------------------------------------------------------+%n");
		System.out.printf("\t\t\t|\t\t                     MANAGE ITEM CATEGORIES                              |%n");
		System.out.printf("\t\t\t+---------------------------------------------------------------------------------+%n"+"\n");
		
		System.out.println();
		System.out.print("[1]Add New Item Category");
		System.out.println("\t\t\t\t\t\t[2]Delete Item Category");
		System.out.print("[3]Update Item Category");
		System.out.println("\t\t\t\t\t\t\t[4]Stock Management");
		System.out.println();
		
		System.out.print("Enter an option to continue->");
		int num = input.nextInt();
		
		if (num==1)
		{
		clearConsole();
		addNewItemCategory();
		}
		if (num==2)
		{
		clearConsole();
		deleteItemCategory();
		}
		if (num==3)
		{
		clearConsole();
		updateItemCategory();
		}
		if (num==4)
		{
		clearConsole();
		StockManage();
		}
		
		}
	public static void SupplierManage(){
	Scanner input = new Scanner(System.in);	
		System.out.printf("+----------------------------------------------------------------+%n");
		System.out.printf("|                        SUPPLIER MANAGE                         |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
		
		System.out.printf("[1] Add Supplier");
		System.out.printf("%40s","[2] Update Supplier");
		System.out.printf("\n"+"[3] Delete Supllier");
		System.out.printf("%35s","[4] View Supllier");
		System.out.printf("\n"+"[5] Search Supplier");
		System.out.printf("%32s","[6] Home Page"+"\n");
		System.out.print("\n"+"Enter an option to continue > ");
		
			int option = input.nextInt();
			
				if(option==1){
				clearConsole();
				AddSupplier();
				} 
				
				if(option==2){
				clearConsole();
				updateSupplier();
				}
				
				if(option==3){
				clearConsole();
				deleteSupplier();
				}

				if(option==4){
		
				clearConsole();
				viewSupplier();
				}
				
				if(option==5){
				clearConsole();
				searchSupplier();
				}
				
				if(option==6){
				clearConsole();
				stockManagement();
				}	
	}	
		
	public static void AddSupplier(){
	Scanner scanner = new Scanner(System.in);	
		System.out.printf("+----------------------------------------------------------------+%n");
		System.out.printf("|                          ADD SUPPLIER                          |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
	
			
			
        boolean addAnotherSupplier = true;
        while (addAnotherSupplier) {
            System.out.printf("%1s %5s","Supplier ID",":"+" ");
            String inputSupplierId = scanner.nextLine();
            

            if (supplierIdExists(inputSupplierId)) {
                System.out.printf("already exists. try another supplier id!"+"\n"+"\n");
                continue;
            }
			
			while(true){
			System.out.printf("%1s %3s","Supplier Name",":"+" ");
            String inputSupplierName = scanner.nextLine();
		
            addSupplier(inputSupplierId , inputSupplierName);
            System.out.print("added successfully! Do you want to add another supplier(Y/N)? ");
            String choice = scanner.nextLine();
					if (!choice.equals("Y")) {
						addAnotherSupplier = false;
                
					}else{
						clearConsole();
						AddSupplier();
						}
					if (!choice.equals("y")) {
						addAnotherSupplier = false;
               
					}else{
						clearConsole();
						AddSupplier();
						}
			
					if(choice.equals("N")){
						clearConsole();
						SupplierManage();
					}
					if(choice.equals("n")){
						clearConsole();
						SupplierManage();
					}
				
			}
		}

        
    }

    private static boolean supplierIdExists(String inputSupplierId) {
        for (int i = 0; i < numSuppliers; i++) {
            if (supplierIds[i].equals(inputSupplierId)) {
                return true;
            }
        }
        return false;
    }

    private static void addSupplier(String inputSupplierId, String inputSupplierName) {
        if (numSuppliers >= supplierIds.length) {
            resizeArrays();
        }

        supplierIds[numSuppliers] = inputSupplierId;
        supplierNames[numSuppliers] = inputSupplierName;
        numSuppliers=numSuppliers+1;
    }

    private static void resizeArrays() {
        int newCapacity = supplierIds.length+1;

        String[] newSupplierIds = new String[newCapacity];
        String[] newSupplierNames = new String[newCapacity];

        for (int i = 0; i < supplierIds.length; i++) {
            newSupplierIds[i] = supplierIds[i];
            newSupplierNames[i] = supplierNames[i];
        }

        supplierIds = newSupplierIds;
        supplierNames = newSupplierNames;
    }


	public static void updateSupplier(){
	Scanner scanner = new Scanner(System.in);	
		
		System.out.printf("+----------------------------------------------------------------+%n");
		System.out.printf("|                          UPDATE SUPPLIER                       |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
	
			
		while (true) {
            System.out.printf("%1s %4s","Supplier ID",":"+" ");
            String inputUpdate = scanner.nextLine();
            
            int count = 0;
            for(int i=0 ; i < supplierIds.length ;i++ ){
				
				if(supplierIds[i].equals(inputUpdate)){
					count=count+1;
					System.out.printf("%1s %6s","Supplier Name",":"+" "+supplierNames[i]+"\n"+"\n");
					System.out.print("Enter the new supplier name: ");
					String newName = scanner.nextLine();
					supplierNames[i]=newName;
					System.out.print("\n"+"Updated Successfully! Do you want to update another supplier?(Y/N) ");
					String YesNo = scanner.nextLine();
					
					if ("Y".equals(YesNo)) {
					clearConsole();
					updateSupplier();
					}
					
					if ("y".equals(YesNo)) {
					clearConsole();
					updateSupplier();
					}else{
						clearConsole();
						SupplierManage();
						}
						
				}
			}	
					if(0==count){
						System.out.print("can't find supplier id. try again!\n\n");
					}
					
		}
		
	}

	private static void deleteSupplier(){
	Scanner scanner = new Scanner(System.in);
		
		System.out.printf("+----------------------------------------------------------------+%n");
		System.out.printf("|                          DELETE SUPPLIER                       |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
	
			if(0==numSuppliers){
				System.out.print("Not found suppliers details!!..Do you want go supplier manage page (Y)?");
				String gobackmanage = scanner.nextLine();
			if("y".equals(gobackmanage)){
				clearConsole();
				SupplierManage();
			}
			if("Y".equals(gobackmanage)){
				clearConsole();
				SupplierManage();
			}
		
			}else
			{
	
				while(true){
					System.out.printf("%1s %5s","Supplier ID",":"+" ");
					String deleteId = scanner.nextLine();

						int index = findSupplierIndex(deleteId);
							if (index != -1) {
								for (int i = index; i < numSuppliers - 1; i++) {
									supplierIds[i] = supplierIds[i + 1];
									supplierNames[i] = supplierNames[i + 1];
								}
								numSuppliers--;
								if(0==numSuppliers){
									System.out.print("deleted successfully!"+"\n"+"All suppliers You deleted !!..Do you want go Supplier Manage Page (Y)?");
									String choice = scanner.nextLine();
								if("y".equals(choice)){
									clearConsole();
									SupplierManage();
								}
								if("Y".equals(choice)){
									clearConsole();
									SupplierManage();
								}
					
								}
							System.out.print("deleted successfully!"+" "+"Do you want to delete another?(Y/N) ");
							String yesno = scanner.nextLine();
							if("Y".equals(yesno)){
								clearConsole();
								deleteSupplier();
							}
							if("y".equals(yesno)){
								clearConsole();
								deleteSupplier();
							}else{
								clearConsole();
								SupplierManage();
							}	
				
            
							}else{
							System.out.println("can't find supplier id. try again!\n");
							}
        
				}
		}
			
    }

    private static int findSupplierIndex(String deleteId) {
		
        for (int i = 0; i < numSuppliers; i++) {
            if (supplierIds[i].equals(deleteId)) {
                return i;
            }
        }
        return -1;
    }
	
	public static void viewSupplier(){
	Scanner scanner = new Scanner(System.in);	
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                             VIEW SUPPLIERS                           |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");
	
		System.out.printf("+---------------------+---------------------+%n");
		System.out.printf("|     SUPPLIER ID     |    SUPPLIER NAME    |%n");
		System.out.printf("+---------------------+---------------------+%n");
	
	
		for(int i =0;i<supplierIds.length;i++){
			System.out.printf("%s %9s %11s %10s %10s %n","|",supplierIds[i],"|",supplierNames[i],"|");
			}
			System.out.printf("+---------------------+---------------------+%n");
			
			System.out.print("Do you want to go supplier manage page(Y/N)? ");
			String choice = scanner.nextLine();
				if("Y".equals(choice)){
					clearConsole();
					SupplierManage();
				}
				if("y".equals(choice)){
					clearConsole();
					SupplierManage();
				}else{
					clearConsole();
					viewSupplier();
				}
	}
    		
    public static void	searchSupplier(){
	Scanner scanner = new Scanner(System.in);	
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                              SEARCH SUPPLIER                         |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");
	
			if(0==numSuppliers){
				System.out.print("Can't search suppliers Details!!..Do you want go Supplier Manage Page (Y)?");
				String choice = scanner.nextLine();
					if("y".equals(choice)){
						clearConsole();
						SupplierManage();
						}
					
					if("Y".equals(choice)){
						clearConsole();
						SupplierManage();
						}else{
							clearConsole();
							searchSupplier();
						}
			}else{
				while(true){
					System.out.printf("%1s %4s","Supplier ID",":"+" ");
					String searchId = scanner.nextLine();
				
						int findCount=0;
							for(int i =0; i<numSuppliers ;i++){
								if(supplierIds[i].equals(searchId)){
									findCount+=1;
									System.out.printf("%1s %3s","Supplier Name",":"+" "+supplierNames[i]+"\n");
									System.out.print("added successfully! Do you want to add another find(Y/N)? ");
										String choiceAdd = scanner.nextLine();
											if("Y".equals(choiceAdd)){
												clearConsole();
												searchSupplier();
											}
											if("y".equals(choiceAdd)){
												clearConsole();
												searchSupplier();
											}else{
												clearConsole();
												SupplierManage();
											}
								}
						}if(0==findCount){
							System.out.print("can't find supplier id. try again!\n\n");
						}
				}
			}
	}
	
	public static void manageItem(){
	Scanner scanner = new Scanner(System.in);
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                          MANAGE ITEM CATEGORY                        |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");	
		
		System.out.printf("[1] Add New Item Category");
		System.out.printf("%30s","[2] Delete Item Category");
		System.out.printf("\n"+"[3] Update Item Category");
		System.out.printf("%27s","[4] Stock Management");
		System.out.print("\n"+"\n"+"Enter an option to continue > ");

		int option = scanner.nextInt();
			
			if(1==option){
				clearConsole();
				addNewItemCategory();
			}
			if(2==option){
				clearConsole();
				deleteItemCategory();
			}
			if(3==option){
				clearConsole();
				updateItemCategory();
			}
			if(4==option){
				clearConsole();
				StockManage();
			}
	
	}	
		
	public static void addNewItemCategory(){
	Scanner scanner = new Scanner(System.in);
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                             ADD ITEM CATEGORY                        |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");
	
	

       while(true){
            System.out.print("Enter the new item category: ");
            String category = scanner.nextLine();
				if (exists(category)) {
					System.out.println("Category already exists. Try another item category!\n");
				} else {
					addItemCategory(category);
					
					System.out.print("added successfully!"+" "+"Do you want to add another category(Y/N)? ");
					String choice = scanner.nextLine();
						if("Y".equals(choice)){
							clearConsole();
							addNewItemCategory();
						}
						if("y".equals(choice)){
							clearConsole();
							addNewItemCategory();
						}else{
							clearConsole();
							StockManage();
						}
				}

       
		}
	}

    public static boolean exists(String category) {
        for (int i = 0; i < itemCount; i++) {
            if (itemCategories[i].equals(category)) {
                return true;
            }
        }
        return false;
    }

    public static void addItemCategory(String category) {
        if (itemCount == itemCategories.length) {
            // Grow the array if it is full
            String[] newArray = new String[itemCategories.length+1];
				for (int i = 0; i < itemCategories.length; i++) {
                newArray[i] = itemCategories[i];
            }
            itemCategories = newArray;
        }

        itemCategories[itemCount] = category;
        itemCount++;
    }


		
		
	public static void deleteItemCategory(){
	Scanner scanner = new Scanner(System.in);
		
		System.out.printf("+----------------------------------------------------------------+%n");
		System.out.printf("|                       DELETE ITEM CATEGORY                     |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
	
				if(0==itemCount){
					System.out.print("Not found item categories!!..Do you want go Add item category Page (Y)?");
					String backItem = scanner.nextLine();
						
						if("y".equals(backItem)){
							clearConsole();
							addNewItemCategory();
						}
						if("Y".equals(backItem)){
							clearConsole();
							addNewItemCategory();
						}
						}else{
							
		
							while(true){
								System.out.printf("%1s %5s","Enter item category Name",":"+" ");
								String deleteItem = scanner.nextLine();

								int index = findItemIndex(deleteItem);
									if (index != -1) {
										for (int i = index; i < itemCount - 1; i++) {
										itemCategories[i] = itemCategories[i + 1];
										}
										
											itemCount--;
											if(0==itemCount){
											System.out.print("deleted successfully!"+"\n"+"All item category You deleted !!..Do you want go Add item category Page (Y)?");
											String choice = scanner.nextLine();
												if("y".equals(choice)){
													clearConsole();
													addNewItemCategory();
												}
												if("Y".equals(choice)){
													clearConsole();
													addNewItemCategory();
												}else{
												clearConsole();
												StockManage();	
												}
					
											}
											System.out.print("deleted successfully!"+" "+"Do you want to delete another?(Y/N) ");
											String yesno = scanner.nextLine();
												if("Y".equals(yesno)){
													clearConsole();
													deleteItemCategory();
												}
												if("y".equals(yesno)){
													clearConsole();
													deleteItemCategory();
												}else{
													clearConsole();
													StockManage();
												}	
				
            
									}else{
										System.out.println("can't find item category. try again!\n");
									}
        
							}
						}	
		
	}

	private static int findItemIndex(String deleteItem) {
		
        for (int i = 0; i < itemCount; i++) {
            if (itemCategories[i].equals(deleteItem)) {
                return i;
            }
        }
        return -1;
    }
	
	
	public static void updateItemCategory(){
	Scanner scanner = new Scanner(System.in);
		
		System.out.printf("+--------------------------------------------------------------------+%n");
		System.out.printf("|                       UPDATE ITEM CATEGORY                     |%n");
		System.out.printf("+----------------------------------------------------------------+%n"+"\n");
	

		if(0==itemCount){
			System.out.print("Not found item categories!!..Do you want go Add item category Page (Y)?");
			String choice=scanner.nextLine();
				if("Y".equals(choice)){
					clearConsole();
					addNewItemCategory();
				}
				if("y".equals(choice)){
					clearConsole();
					addNewItemCategory();
				}
		}else{
				
			while (true) {
				System.out.printf("%1s %5s","Enter item category Name",":"+" ");
				String inputUpdate = scanner.nextLine();
            
				int count = 0;
				for(int i=0 ; i < itemCategories.length ;i++ ){
				
					if(itemCategories[i].equals(inputUpdate)){
						count=count+1;
						System.out.printf("%1s %2s","Enter the new category Name",":"+" ");
						String newName = scanner.nextLine();
					
							itemCategories[i]=newName;
							System.out.print("\n"+"Updated Successfully! Do you want to update another item category?(Y/N) ");
							String YesNo = scanner.nextLine();
					
								if ("Y".equals(YesNo)) {
									clearConsole();
									updateItemCategory();
								}
					
								if ("y".equals(YesNo)) {
									clearConsole();
									updateItemCategory();
								}else{
									clearConsole();
									StockManage();
								}
						
					}
				}	
				if(0==count){
				System.out.print("can't find item category. try again!\n\n");
				}
					
			}
			
		
		
		}
		
	}		
	
	private static void addItem(){
	Scanner scanner = new Scanner(System.in);
	
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                                ADD ITEM                              |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");	
			
		if(0==itemCount){
				System.out.print("OOPS! It seems that you don't have any item categories in the system.\n");
				System.out.print("Do you want to add a new item category?(Y/N)");
				String choice=scanner.nextLine();
					if("Y".equals(choice)){
						clearConsole();
						addNewItemCategory();
					}
					if("y".equals(choice)){
						clearConsole();
						addNewItemCategory();
					}else{
						clearConsole();
						addItem();
					}
		}
			
		if(0==numSuppliers){
				System.out.print("OOPS! It seems that you don't have any suppliers in the system.\n");
				System.out.print("Do you want to add a new supplier?(Y/N)");
					String choice=scanner.nextLine();
					if("Y".equals(choice)){
						clearConsole();
						AddSupplier();
					}
					if("y".equals(choice)){
						clearConsole();
						AddSupplier();
					}else{
						clearConsole();
						addItem();
					}
					
		}
				
		while(true){
            System.out.print("Item Code : ");
            String inputItems = scanner.nextLine();
            
				if (existsItem(inputItems)) {
					System.out.println("Item already exists. Try another item!\n");
				} else {
					int numitem = addItemSystem(inputItems);
					System.out.print("\n"+"Supplier list:"+"\n");
					
					System.out.printf("+-------------+---------------------+---------------------+%n");
					System.out.printf("|      #      |     SUPPLIER ID     |    SUPPLIER NAME    |%n");
					System.out.printf("+-------------+---------------------+---------------------+%n");
		
					for(int i=0; i < numSuppliers;i++){
						System.out.printf("%s %5s %7s %11s %9s %11s %9s%n","|",(i+1),"|",supplierIds[i],"|",supplierNames[i],"|");
					}
					System.out.printf("+-------------+---------------------+---------------------+%n"+"\n");
					int i1 = 0;
					System.out.print("Enter the supplier number > ");
						int numBer = scanner.nextInt();
							for(int i =0 ; i < supplierIds.length ; i++){
								if(numBer==(i+1)){
									i1=i;
								}
							}
					System.out.print("\n"+"Item Categories:"+"\n");
					
						System.out.printf("+-------------+---------------------+%n");
						System.out.printf("|      #      |    CATEGORY NAME    |%n");
						System.out.printf("+-------------+---------------------+%n");
						
						for(int i=0; i < itemCategories.length;i++){
							System.out.printf("%s %5s %7s %11s %10s","|",(i+1),"|",itemCategories[i],"|"+"\n");
						}		
							System.out.printf("+-------------+---------------------+%n"+"\n");
								int i2 =0;	
								System.out.print("Enter the category number > ");
								int nuBer = scanner.nextInt();
						for(int j =0 ; j < itemCategories.length ; j++){
							if(nuBer==(j+1)){
								i2=j;
							}
						}
						
						addSuppItem(i1,i2,inputItems);
						getdetailItem(numitem);
				
				}

       
		}
	}
	
	private static void addSuppItem(int i1,int i2,String inputItems) {
        if (countz >= SuppItem.length) {
            resizeArra();
        }

			SuppItem[countz][0] = supplierIds[i1];
			SuppItem[countz][1] = itemCategories[i2];
			SuppItem[countz][2] = inputItems;
				countz=countz+1;
    }

    private static void resizeArra() {
        int newCapasity = SuppItem.length+1;

        String[][] newSuppItem = new String[newCapasity][3];

        for (int i = 0; i < SuppItem.length; i++) {
            newSuppItem[i][0] = SuppItem[i][0];
            newSuppItem[i][1] = SuppItem[i][1];
            newSuppItem[i][2] = SuppItem[i][2];
        }

			SuppItem = newSuppItem;

    }
	
	

    public static boolean existsItem(String inputItems) {
        for (int i = 0; i < numitem; i++) {
            if (items[i].equals(inputItems)) {
                return true;
            }
        }
        return false;
    }

    private static int addItemSystem(String inputItems) {
	Scanner scanner = new Scanner(System.in);
        if (numitem == items.length) {
            // Grow the array if it is full
            String[] newArray = new String[items.length+1];
            for (int i = 0; i < items.length; i++) {
                newArray[i] = items[i];
            }
            items = newArray;
            
        }

        items[numitem] = inputItems;
        numitem=numitem+1;
   
		return numitem;
    }
    
	private static void getdetailItem(int numitem){
	Scanner scanner = new Scanner(System.in);
	
				System.out.printf("\n"+"%1s %4s","Description",":"+" ");
				String des = scanner.nextLine();
			
				System.out.printf("%1s %5s","Unit price",":"+" ");
				float unit = scanner.nextFloat();
				
				String qty = end();

				itemDetail(des,unit,qty);
				
	}	
	
	private static void itemDetail(String des,float unit,String qty) {
		Scanner scanner = new Scanner(System.in);
		
        if (itemDetailCount >= itemdetails.length) {
            incrementArray();
        }

        itemdetails[itemDetailCount][0] = des;
        price[itemDetailCount]= unit;
        itemdetails[itemDetailCount][1] = qty;
		itemDetailCount=itemDetailCount+1;

		
		System.out.print("added successfully!"+" "+"Do you want to add another item(Y/N)? ");
		String choice = scanner.nextLine();
				if("Y".equals(choice)){
					clearConsole();
					addItem();
				}
				if("y".equals(choice)){
					clearConsole();
					addItem();
				}else{
					clearConsole();
					StockManage();
				
				}
			
    }

    private static void incrementArray() {
        int newCountx = itemdetails.length+1;


        String[][] newItemDetail = new String[newCountx][2];
        float [] newpriceCount = new float[newCountx];

        for (int i = 0; i < itemdetails.length; i++) {
            newItemDetail[i][0] = itemdetails[i][0];
            newItemDetail[i][1] = itemdetails[i][1];
			newpriceCount[i] = price[i];
        }

        itemdetails=newItemDetail;
		price = newpriceCount;
    }
		
	public static String end(){
	Scanner scanner = new Scanner(System.in);
	
				System.out.printf("%1s %4s","Qty on hand",":"+" ");
				String qty = scanner.nextLine();
				return qty;
				
	}
	
	public static void getItems(){
	Scanner scanner = new Scanner(System.in);
	
			System.out.printf("+----------------------------------------------------------------------+%n");
			System.out.printf("|                      SEARCH ITEMS SUPPLIER WISE                      |%n");
			System.out.printf("+----------------------------------------------------------------------+%n"+"\n");	
			
			System.out.printf("%1s %5s","Supplier ID",":"+" ");
			String inputId = scanner.nextLine();
			
				int count = 0;
					for(int k =0; k< supplierIds.length;k++){
						if(inputId.equals(supplierIds[k])){
							count=count+1;
						}
					}
			
	
				if(0<count){
			
					for(int i =0; i<supplierIds.length;i++){
							if(inputId.equals(supplierIds[i])){
							System.out.print("Supplier Name : "+supplierNames[i]+"\n"+"\n");
						
									System.out.printf("+---------------+-------------------+------------------+-------------------+----------------+%n");
									System.out.printf("|   ITEM CODE   |    DESCRIPTION    |    UNIT PRICE    |    QTY ON HAND    |    CATEGORY    |%n");
									System.out.printf("+---------------+-------------------+------------------+-------------------+----------------+%n");
								
										for(int y =0 ; y < SuppItem.length ; y++){
											if(inputId.equals(SuppItem[y][0])){
										
												for(int j =0 ; j < items.length ; j++){
													if(SuppItem[y][2].equals(items[j])){
													System.out.printf("|    %-11s|    %-15s|    %-14s|    %-15s|    %-12s|%n",SuppItem[y][2],itemdetails[j][0],price[j],itemdetails[j][1],SuppItem[y][1]);
													}
											
												}
											}
										}
								System.out.printf("+---------------+-------------------+------------------+-------------------+----------------+"+"\n");
							}
					}

						System.out.print("search successfully! Do you want to another search?(Y/N) ");
						String yes = scanner.nextLine();
							if("y".equals(yes)){
								clearConsole();
								getItems();
							}
							if("Y".equals(yes)){
								clearConsole();
								getItems();
							}else{
								clearConsole();
								StockManage();
							}
				}else{
							System.out.print("Invalid supplier id! Do you want try again (Y)?");
							String choice = scanner.nextLine();
							if("y".equals(choice)){
								clearConsole();
								getItems();
							}
							if("Y".equals(choice)){
								clearConsole();
								getItems();
							}
						}
		
	}
		
	public static void viewItem(){
	Scanner scanner = new Scanner(System.in);
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                               VIEW ITEMS                             |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");	
			
		
		
		for(int i=0 ; i<itemCategories.length;i++){
			System.out.print(itemCategories[i]+":"+"\n");
				System.out.printf("+--------------+------------+------------+-------------+-----------+%n");
				System.out.printf("|    SID       |    CODE    |    DESC    |    PRICE    |    QTY    |%n");
				System.out.printf("+--------------+------------+------------+-------------+-----------+%n");
		
			for(int j =0 ; j <  countz ; j++){
				 if(itemCategories[i].equals(SuppItem[j][1])){
					System.out.printf("|    %-10s|    %-8s|    %-8s|    %-9s|    %-7s|%n", SuppItem[j][0], SuppItem[j][2], itemdetails[j][0], price[j], itemdetails[j][1]);
					}
				
				}
				
				System.out.print("+--------------+------------+------------+-------------+-----------+"+"\n"+"\n");
			
		}
		
		System.out.print("Do you want to go stock manage page ?(Y/N)");
				String yes = scanner.nextLine();
					if("y".equals(yes)){
						clearConsole();
						StockManage();
					}
					if("Y".equals(yes)){
						clearConsole();
						StockManage();
					}else{
						clearConsole();
						viewItem();
					}
	}
	
	public static void rankItem(){
	Scanner scanner = new Scanner(System.in);
		System.out.printf("+----------------------------------------------------------------------+%n");
		System.out.printf("|                             RANKED UNIT PRICE                        |%n");
		System.out.printf("+----------------------------------------------------------------------+%n"+"\n");	
			
			System.out.println();
		
		
				System.out.printf("+--------------+------------+------------+-------------+-----------+------------+%n");
				System.out.printf("|    SID       |    CODE    |    DESC    |    PRICE    |    QTY    |    CAT     |%n");
				System.out.printf("+--------------+------------+------------+-------------+-----------+------------+%n");
	
			int count = 0;
			float[] newz = new float[price.length];
			
			for(int i =0 ; i < price.length ; i++){
					newz[i]=price[i];
					//count=count+1;
			} 
				
			for (int i = 0; i < newz.length - 1; i++) {
				for (int j = i + 1; j <newz.length; j++) {
					if (newz[i] > newz[j]) {
						float temp = newz[i];
						newz[i] = newz[j];
						newz[j] = temp;
					}
				}
			}

      
       for (int i = 0; i < newz.length; i++) {
			
			for(int j =0 ; j < price.length; j++){
				
				if(newz[i]==(price[j])){
					
				System.out.printf("|    %-10s|    %-8s|    %-8s|    %-9s|    %-7s|    %-8s|%n",SuppItem[j][0],SuppItem[j][2],itemdetails[j][0],newz[i],itemdetails[j][1],SuppItem[j][1]);
					
				}else{
				}
			
			
			}
		}
	
			System.out.printf("+--------------+------------+------------+-------------+-----------+------------+%n");
				
				System.out.print("Do you want to go stock manage page?(Y/N) ");
				String yes = scanner.nextLine();
					if("y".equals(yes)){    
						clearConsole();
						StockManage();
					}
					if("Y".equals(yes)){
						clearConsole();
						StockManage();
					}else{
						clearConsole();
						rankItem();
					}
						
	}
	public static void main(String args[]){
		usernamepassword();
		clearConsole();
		stockManagement();
		stockManagementOption();
		
	
		}
	
		
	}

