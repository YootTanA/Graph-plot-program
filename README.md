# Graph-plot-program
#This is a basic program for plot graph
import matplotlib.pyplot as plt

def graph_plot(x,y):
    plt.plot(x,y)
    plt.show()
def graph_name(name):
    plt.title(name)
def graph_label(xLa,yLa):
    plt.xlabel(xLa)
    plt.ylabel(yLa)

while(True):
    n = int(input("press button 1 for plot graph \npress button 2 for end a program\n:"))
    if(n==1):

      while(True):
          yes_no_quest = input("Do you want to name your graph(yes/no)?\n:")
          if(yes_no_quest=='Yes' or yes_no_quest=='yes'):
              nameG = input('Input your graph\'s name\n:')
              graph_name(nameG)
              break
          elif(yes_no_quest=='No' or yes_no_quest=='no'):
              print("ok let plot a graph with out name \n")
              break
          else:
              print("Wrong input!! Try again")

      while(True):      
          yes_no_quest2= input("Do you want to name xlabels and ylabels(yes/no)?\n:")
          if(yes_no_quest2 =='Yes' or yes_no_quest2=='yes'):
              name_xla = input('Input your xlabel name\n:')
              name_yla = input('Input your ylabel name\n:')
              graph_label(name_xla,name_yla)
              break
          elif((yes_no_quest=='No' or yes_no_quest=='no') and (yes_no_quest2=='no' or yes_no_quest2=='No')):
              print("ok let plot a graph with out name, xlabels and ylabels")
              break
          elif((yes_no_quest=='Yes' or yes_no_quest=='yes') and (yes_no_quest2=='no' or yes_no_quest2=='No')):
              print("ok let plot a graph with out xlabels and ylabels")
              break
          else:
              print("Wrong input!! Try again")
     
      x = [int(i) for i in input("Enter X:").split()]
      y = [int(j) for j in input("Enter y:").split()]
      graph_plot(x,y)
      
    elif(n==2):
        print("thank for using program")
        break
    else:
        print("you input wrong number")
