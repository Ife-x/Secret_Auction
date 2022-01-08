# Secret_Auction
from replit import clear
logo = ('''
                         ___________
                         \         /
                          )_______(
                          |"""""""|_.-._,.---------.,_.-._
                          |       | | |               | | ''-.
                          |       |_| |_             _| |_..-'
                          |_______| '-' `'---------'` '-'
                          )"""""""(
                         /_________\\
                       .-------------.
                      /_______________\\
''')
print(logo)
auction_detail = {}
bidding_ends = False
def highest_bidder(bids_record):
  highest_bid = 0
  winner = " "


  for bids in bids_record:
    bid_amount = bids_record[bids]
    if bid_amount > highest_bid:
      highest_bid = bid_amount
      winner = bids
  print(f'The winner is {winner} with a bid of ${highest_bid}')


while not bidding_ends:
  name = input('What is your name?\n')
  bid_amount = int(input('How much are you bidding?\n $'))
  auction_detail[name] = bid_amount
  continue_bidding = input('Are there other bidders? Type "Yes" or Type "No"\n')
  if continue_bidding == "No":
    bidding_ends = True
    highest_bidder(auction_detail)
  elif continue_bidding == "Yes":
    clear()
