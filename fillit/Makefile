# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: sdiego <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/09/29 15:20:36 by sdiego            #+#    #+#              #
#    Updated: 2019/09/30 12:40:35 by sdiego           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = fillit

SRC = ./src/main.c ./src/read.c ./src/solve.c ./src/tetri.c

OBJ = $(SRC:.c=.o)

INCLUDES = ./includes

all: $(NAME)

$(NAME): $(OBJ)
	make -C ./libft/
	gcc -Wall -Wextra -Werror -o $(NAME) $(OBJ) ./libft/src/*.o -I$(INCLUDES)

.c.o:
	gcc -Wall -Wextra -Werror -I./$(INCLUDES) -c $< -o $@

clean:
	make clean -C ./libft/
	/bin/rm -f $(OBJ)

fclean: clean
		/bin/rm -f $(NAME)
		make fclean -C ./libft/

re: fclean all
