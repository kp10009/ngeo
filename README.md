# ngeo
college = input("Enter a college class:")
AD = input("Enter the adjustive:")
sport = input("Enter an activity:")
print(college + " class was really "+ AD +" today. We learn how to " + sport+
     " today in class. I can't wait for tomorrow's class!")
print("Enter your scores:\n")
scores = [int(x) for x in input().split()]
scores_ = scores
#highest and lowest and average
def check(scores):
    sum =0
    a = scores[0]
    b = scores[0]
    nb = 0
    for i in range(len(scores)):
        if scores[i] <= a :
            a = scores[i]
        if b <= scores[i] :
            b = scores[i] 
            nb = i
            sum += scores[i]
    return a, b, nb, sum
print("The lowest score: "+ str(check(scores)[0]) +"\n")
print("The highest score:" +str(check(scores)[1]) + "\n")        
print("The average score:" +str(check(scores)[3]/len(scores))+"\n")
#the second highest
b = check(scores)[1]
scores_.remove(b)
b_ = scores_[0]
for i in range(len(scores_)):
    if b_ <= scores_[i] :
        b_ = scores_[i] 
print("The second highest is: " +str(b_))
#warning >100
for i in range(len(scores)):
    if  scores[i]>100:
        print("Warning: you entered not permit score, score is greater 100")
        break
#drop low+average
scores_ = list(filter(lambda a: a != check(scores)[0], scores))
scores_ = list(filter(lambda a: a != check(scores)[0], scores))
print("The average score_ :" +str(check(scores)[3]/len(scores))+"\n")
